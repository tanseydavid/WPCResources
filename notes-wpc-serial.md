Notes - WPC Serial Support
==========================

> Each NULL modem has built-in support for the 'bitbanger' and dies translation between the stream and the selected baudrate

> NULL modem "bitbanger" accepts a socket address as an argument


```
ASCII   5  0x05  <CTRL-E>   ENQ  
ASCII  13  0c0D  <CTRL-M>   CR
ASCII  17  0x11  <CTRL-Q> 	XON   DC1  
ASCII  19  0x13  <CTRL-S>	  XOFF  DC3  
```


### DMD Image Support

```
// DMD.cpp : implementation file
//

#include "stdafx.h"
#include "defines.h"
#include "HexEditor.h"
#include "DMD.h"
#include "hexeditordoc.h"
#include "hexeditorview.h"
#include "mybutton.h"
#include "nagdlg.h"
#include "version.h"

time_t actTime;

#ifdef _DEBUG
#define new DEBUG_NEW
#undef THIS_FILE
static char THIS_FILE[] = __FILE__;
#endif


#define ALLOW_MOUSE_TO_REPEAT    (0)

//
// WPC Games
// -----------------------------------------------------------------------
// Addams Family L5, H4
// Addams Family Gold H3
// Attack From Mars 1.13
// Black Rose L3
// Cactus Canyon 1.3              **8 MEG**
// Champion Pub 1.6
// Cirqus Voltaire 1.4            **8 MEG**
// Congo 2.1
// Corvette 2.1
// Creature from the black lagoon L4
// Demolition Man LX4
// Dirty Harry LX2
// Dracula L1
// Dr. Who L2
// Fish Tales L5
// Flintstones LX5
// Gilligans Island L9
// Getaway High Speed II L5
// Hurricane L2
// Indiana Jones L7
// Indianopolis 500 1.1R
// Jackbot 1.0R
// Johnny Mnemonic 1.2R
// Judge Dredd L7
// Junkyard 1.2
// Medievil Madness 1.09H         **8 MEG**
// Monster Bash 1.06
// NBA Fastbreak 3.1
// No Fear 2.3X
// No Good Gofers 1.3
// Popeye LX5
// Roadshow L6
// Safe Cracker 1.8G
// Scared Stiff 1.5
// Shadow LX6
// Slugfest L1
// Star Trek Next Generation L7
// Tales of the Arabian Nights 1.4
// Terminator 2 L8
// Theater of Magic 1.3
// Ticket Tac Toe 1.0
// Twilight Zone 9.4H
// White Water L5
// Who Dunnit 1.2
// World Cup Soccer LX2
//
//
// WPC, but no DMD!
// ----------------
// Dr. Dude
// Funhouse
// Harley Davidson
// League Champ
// Party Zone
// Strike Master
// The Machine Bride of Pinbot
// 
// 
//
//
/////////////////////////////////////////////////////////////////////////////
// DMD dialog


DMD::DMD(CWnd* pParent /*=NULL*/,RegistrySettings *mainptr, int DialogType)
	: CDialog(DMD::IDD, pParent)
{
	PassedInPointer = mainptr;
	NaggedOnce = 0;
	dialogType = DialogType;
	//{{AFX_DATA_INIT(DMD)
	//}}AFX_DATA_INIT
}

DMD::~DMD()
{
}
void DMD::DoDataExchange(CDataExchange* pDX)
{
	CDialog::DoDataExchange(pDX);
	//{{AFX_DATA_MAP(DMD)
	DDX_Control(pDX, IDC_BUTTON_WIPE, m_Wipe);
	DDX_Control(pDX, IDC_BUTTON_PREVIOUS_GRAPHICX2, m_PreviousGraphicX2);
	DDX_Control(pDX, IDC_BUTTON_NEXT_GRAPHICX2, m_NextGraphicX2);
	DDX_Control(pDX, IDC_CHECK_EXPORT, m_Export);
	DDX_Control(pDX, IDC_STATIC_DMD3_HEADER, m_Dmd3Title);
	DDX_Control(pDX, IDC_STATIC_DMD2_HEADER, m_Dmd2Title);
	DDX_Control(pDX, IDC_STATIC_DMD1_HEADER, m_Dmd1Title);
	DDX_Control(pDX, IDC_SPIN1, m_Spin);
	DDX_Control(pDX, IDC_LIST1, m_PixelColor);
	DDX_Control(pDX, IDC_CHECK_XORED, m_Xored);
	DDX_Control(pDX, IDC_CHECK_SKIPPED, m_Skipped);
	DDX_Control(pDX, IDC_STATIC_DMD1_TEXTBOX, m_Dmd1);
	DDX_Control(pDX, IDC_STATIC_DMD2_TEXTBOX, m_Dmd2);
	DDX_Control(pDX, IDC_STATIC_DMD3_TEXTBOX, m_Dmd3);
	DDX_Control(pDX, IDC_BUTTON_NEXT_GRAPHIC, m_NextGraphic);
	DDX_Control(pDX, IDC_BUTTON_PREVIOUS_GRAPHIC, m_PreviousGraphic);
	DDX_Control(pDX, IDC_STATIC_USERREG, m_UserReg);
	//}}AFX_DATA_MAP
}


BEGIN_MESSAGE_MAP(DMD, CDialog)
	//{{AFX_MSG_MAP(DMD)
	ON_WM_CREATE()
	ON_WM_DESTROY()
	ON_WM_PAINT()
	ON_BN_CLICKED(IDC_BUTTON_NEXT_GRAPHIC, OnButtonNextGraphic)
	ON_BN_CLICKED(IDC_BUTTON_PREVIOUS_GRAPHIC, OnButtonPreviousGraphic)
	ON_BN_CLICKED(IDC_CHECK_SKIPPED, OnCheckSkipped)
	ON_BN_CLICKED(IDC_CHECK_XORED, OnCheckXored)
	ON_BN_CLICKED(IDC_CHECK_EXPORT, OnCheckExport)
	ON_LBN_SELCHANGE(IDC_LIST1, OnSelchangeList1)
	ON_WM_CLOSE()
	ON_WM_CTLCOLOR()
	ON_WM_SHOWWINDOW()
	ON_WM_TIMER()
	ON_WM_LBUTTONDOWN()
	ON_WM_LBUTTONUP()
	ON_BN_CLICKED(IDC_BUTTON_NEXT_GRAPHICX2, OnButtonNextGraphicx2)
	ON_BN_CLICKED(IDC_BUTTON_PREVIOUS_GRAPHICX2, OnButtonPreviousGraphicx2)
	ON_BN_CLICKED(IDC_BUTTON_WIPE, OnButtonWipe)
	//}}AFX_MSG_MAP
END_MESSAGE_MAP()

/////////////////////////////////////////////////////////////////////////////
// DMD message handlers

BOOL DMD::Create() 
{
	return CDialog::Create(DMD::IDD);
}

BOOL DMD::Create(LPCTSTR lpszClassName, LPCTSTR lpszWindowName, DWORD dwStyle, const RECT& rect, CWnd* pParentWnd, UINT nID, CCreateContext* pContext) 
{
	return CDialog::Create(IDD, pParentWnd);
}

int DMD::OnCreate(LPCREATESTRUCT lpCreateStruct) 
{
	if (CDialog::OnCreate(lpCreateStruct) == -1)
	{
		return -1;
	}
	return 0;
}

void DMD::OnDestroy() 
{
	CDialog::OnDestroy();
}

void DMD::DebugKeyMsgStrPrint(CString str, int KeyMask)
{
	if (debugKeyBitmask & KeyMask)
	{
		if (AfxMessageBox(str,(MB_OKCANCEL | MB_ICONQUESTION)) == IDCANCEL)
		{
			// 'Cancel' stops further debug messages
			debugKeyBitmask &= ~KeyMask;
		}
	}
}

void DMD::DebugShiftKeyMsgStrPrint(CString str)
{
	DebugKeyMsgStrPrint(str, DEBUG_KEY_BIT_SHIFTKEYS);
}

void DMD::DebugControlKeyMsgStrPrint(CString str)
{
	DebugKeyMsgStrPrint(str, DEBUG_KEY_BIT_CONTROLKEYS);
}

BOOL DMD::OnInitDialog() 
{
	int WindowVerticalShift = 0;
	int WindowHorizontalShift = 0;

	CDialog::OnInitDialog();
	
	m_PixelColor.AddString("Black&White");
	m_PixelColor.AddString("Red");
	m_PixelColor.AddString("Yellow");
	m_PixelColor.AddString("Green");
	m_PixelColor.AddString("Teal");
	m_PixelColor.AddString("Blue");
	m_PixelColor.AddString("Violet");
	m_PixelColor.SetTopIndex(PassedInPointer->PixelColor);
	m_Spin.SetPos(PassedInPointer->PixelColor);
/* // default: no checkbox, We now save previous frame pixel data
	m_Xored.SetCheck(PassedInPointer->XoredCheckboxState);
	m_Skipped.SetCheck(PassedInPointer->SkippedCheckboxState);
*/

	CString RegString;
	RegString.Format("%s %.1f %s %s",APPLICATION_TITLE,APPLICATION_VERSION,APPLICATION_COPYRIGHT,APPLICATION_AUTHOR);
	m_UserReg.SetWindowText(RegString);

	switch (dialogType)
	{
		case DMD_DIALOG_TYPE_GRAPHICS:
			SetWindowText("Dot Matrix Display, Full Frame Graphic Data");
			GetDlgItem(IDC_STATIC_DMD1_HEADER)->SetWindowText("Medium Pixels Plane");
			GetDlgItem(IDC_STATIC_DMD2_HEADER)->SetWindowText("Dim Pixels Plane");
			GetDlgItem(IDC_STATIC_DMD3_HEADER)->SetWindowText("Blended Planes");
			GetDlgItem(IDC_BUTTON_PREVIOUS_GRAPHIC)->SetWindowText("<- Prev");
			GetDlgItem(IDC_BUTTON_NEXT_GRAPHIC)->SetWindowText("Next ->");
			GetDlgItem(IDC_CHECK_XORED)->ShowWindow(SW_SHOW);
			GetDlgItem(IDC_CHECK_SKIPPED)->ShowWindow(SW_SHOW);
			WindowVerticalShift = 30;
			WindowHorizontalShift = 20;
			break;

		case DMD_DIALOG_TYPE_FONTDATA:
			SetWindowText("Dot Matrix Display, Font Data");
			GetDlgItem(IDC_BUTTON_PREVIOUS_GRAPHIC)->SetWindowText("<--Previous Char");
			GetDlgItem(IDC_BUTTON_NEXT_GRAPHIC)->SetWindowText("Next Char -->");
			GetDlgItem(IDC_CHECK_XORED)->ShowWindow(SW_HIDE);
			GetDlgItem(IDC_CHECK_SKIPPED)->ShowWindow(SW_HIDE);
			GetDlgItem(IDC_CHECK_XORED)->ShowWindow(SW_HIDE);
			GetDlgItem(IDC_CHECK_SKIPPED)->ShowWindow(SW_HIDE);
			WindowVerticalShift = 80;
			WindowHorizontalShift = 60;
			break;

		case DMD_DIALOG_TYPE_ANIDATA:
			SetWindowText("Dot Matrix Display, Animation Data");
			GetDlgItem(IDC_BUTTON_PREVIOUS_GRAPHIC)->SetWindowText("<--Previous Frame");
			GetDlgItem(IDC_BUTTON_NEXT_GRAPHIC)->SetWindowText("Next Frame -->");
			GetDlgItem(IDC_CHECK_XORED)->ShowWindow(SW_HIDE);
			GetDlgItem(IDC_CHECK_SKIPPED)->ShowWindow(SW_HIDE);
			GetDlgItem(IDC_CHECK_XORED)->ShowWindow(SW_HIDE);
			GetDlgItem(IDC_CHECK_SKIPPED)->ShowWindow(SW_HIDE);
			WindowVerticalShift = 130;
			WindowHorizontalShift = 100;
			break;

		default:
			AfxMessageBox("Error, unrecognized dialogType!");
			break;
	}

	if ((WindowHorizontalShift != 0) || (WindowVerticalShift != 0))
	{
		WINDOWPLACEMENT wp;
		if (GetWindowPlacement(&wp))
		{
			SetWindowPos(NULL, (wp.rcNormalPosition.left + WindowHorizontalShift), (wp.rcNormalPosition.top + WindowVerticalShift),0,0,SWP_NOSIZE);
		}
	}

//    m_PreviousGraphicX2.SetWindowText("2<<");
//    m_NextGraphicX2.SetWindowText(">>2");
    m_PreviousGraphicX2.SetIcon(::LoadIcon(AfxGetInstanceHandle(), MAKEINTRESOURCE(IDI_ICON3)));
    m_NextGraphicX2.SetIcon(::LoadIcon(AfxGetInstanceHandle(), MAKEINTRESOURCE(IDI_ICON2)));

    m_Wipe.SetIcon(::LoadIcon(AfxGetInstanceHandle(), MAKEINTRESOURCE(IDI_ICON1)));
	m_Wipe.EnableWindow(FALSE);
    bWiped = FALSE;


#if ALLOW_MOUSE_TO_REPEAT
	TimerIDDMD = SetTimer(TIMER_DMD, TIMER_DMD_UPDATE, NULL);
	NextDebounce =
	PreviousDebounce = 0;
	NextDebounceState =
	PreviousDebounceState = DEBOUNCE_STATE_IDLE;
#endif

    // init clipboard selector
    selectedTitleBox = 0;

	memset(PreviousPlaneDataPane0,0,sizeof(PreviousPlaneDataPane0));
	memset(PreviousPlaneDataPane1,0,sizeof(PreviousPlaneDataPane1));

	UpdateControls();

	return TRUE;  // return TRUE unless you set the focus to a control
	              // EXCEPTION: OCX Property Pages should return FALSE
} 

void DMD::PaintDMDPanelImage(CPaintDC *pDc, DMDPlanes* pPlanes, unsigned char PaneMask) 
{
	int i,j,k;
	int RowIndex, ColumnIndex;
    ThisPixel thisPixel0;
    ThisPixel thisPixel1;
	unsigned char ReadMask;
	unsigned char PLANE_BITS;
	unsigned char *Plane_0Ptr      = pPlanes->Plane0.Plane_Data;
	unsigned char *Plane_0XorFlags = pPlanes->Plane0.Plane_XorFlags;
	unsigned char *Plane_0XorBits  = pPlanes->Plane0.Plane_XorBits;
	unsigned char *Plane_0Skipped  = pPlanes->Plane0.Plane_Skipped;
	unsigned char *Plane_1Ptr      = pPlanes->Plane1.Plane_Data;
	unsigned char *Plane_1XorFlags = pPlanes->Plane1.Plane_XorFlags;
	unsigned char *Plane_1XorBits  = pPlanes->Plane1.Plane_XorBits;
	unsigned char *Plane_1Skipped  = pPlanes->Plane1.Plane_Skipped;
    unsigned char *Plane_0Previous = PreviousPlaneDataPane0;
    unsigned char *Plane_1Previous = PreviousPlaneDataPane1;
	unsigned char XoredCheck = m_Xored.GetCheck();
	unsigned char SkippedCheck = m_Skipped.GetCheck();
    BOOL bAnyXoredPixel = FALSE;
    BOOL bAnySkippedPixel = FALSE;

	const int PixelColorIDs[PIXEL_COLORS][PIXEL_SHADES] = 
	{
		IDB_BITMAP_PIXEL_GREYDIM,
		IDB_BITMAP_PIXEL_GREYMEDIUM,
		IDB_BITMAP_PIXEL_GREYBRIGHT,
		IDB_BITMAP_PIXEL_REDDIM,
		IDB_BITMAP_PIXEL_REDMEDIUM,
		IDB_BITMAP_PIXEL_REDBRIGHT,
		IDB_BITMAP_PIXEL_YELLOWDIM,
		IDB_BITMAP_PIXEL_YELLOWMEDIUM,
		IDB_BITMAP_PIXEL_YELLOWBRIGHT,
		IDB_BITMAP_PIXEL_GREENDIM,
		IDB_BITMAP_PIXEL_GREENMEDIUM,
		IDB_BITMAP_PIXEL_GREENBRIGHT,
		IDB_BITMAP_PIXEL_TEALDIM,
		IDB_BITMAP_PIXEL_TEALMEDIUM,
		IDB_BITMAP_PIXEL_TEALBRIGHT,
		IDB_BITMAP_PIXEL_BLUEDIM,
		IDB_BITMAP_PIXEL_BLUEMEDIUM,
		IDB_BITMAP_PIXEL_BLUEBRIGHT,
		IDB_BITMAP_PIXEL_VIOLETDIM,
		IDB_BITMAP_PIXEL_VIOLETMEDIUM,
		IDB_BITMAP_PIXEL_VIOLETBRIGHT
	};

	CDC hOff;
	CDC hXored;
	CDC hSkipped;
	CDC hMedium;
	CDC hDim;
	CDC hBright;

	j = 0;
	j += hOff.CreateCompatibleDC(NULL);
	j += hXored.CreateCompatibleDC(NULL);
	j += hSkipped.CreateCompatibleDC(NULL);
	j += hDim.CreateCompatibleDC(NULL);
	j += hMedium.CreateCompatibleDC(NULL);
	j += hBright.CreateCompatibleDC(NULL);
	if (j != 6)
	{
		AfxMessageBox("Problem loading pixels.");
		return;
	}

    // Init clipboard variables
    LPTSTR cbData=NULL;
    LPTSTR cbPtr=NULL;
    char cbPixel0=0;  // temporarily using as a flag to indicate if we want to use clipboard
    char cbPixel1;
    char cbPixel2;
    switch (selectedTitleBox)
    {
       case 1:
          if (PaneMask & DMD_FULLFRAME_PAINT_MEDIUM)
          {
              cbPixel0++; // flag that we want to use clipboard
          }
          break;
       case 2:
          if (PaneMask & DMD_FULLFRAME_PAINT_DIM)
          {
              cbPixel0++; // flag that we want to use clipboard
          }
          break;
       case 3:
          if (PaneMask & DMD_FULLFRAME_PAINT_BLENDED)
          {
              cbPixel0++; // flag that we want to use clipboard
          }
          break;
       default:
          break;
    }

    if ((cbPixel0 != 0) && (OpenClipboard()) && (EmptyClipboard()))
    {
        cbPtr = cbData = (LPTSTR)LocalAlloc(LPTR,(((DMD_COLUMNS+2)*DMD_ROWS)+1)); // +2 for the newline & linefeed (/r/n) +1 for trailing NULL
    }

	CBitmap BMOff;
	CBitmap BMXored;
	CBitmap BMSkipped;
	CBitmap BMDim;
	CBitmap BMMedium;
	CBitmap BMBright;

	i = m_PixelColor.GetTopIndex();
	if (i > PIXEL_COLORS)
	{
		i = PIXEL_COLORS;
	}

	j = 0;
	j += BMOff.LoadBitmap(IDB_BITMAP_PIXEL_BLACK);
	if (i == NORMAL_XORED_COLOR)
	{
		j += BMXored.LoadBitmap(PixelColorIDs[ALTERNATE_XORED_COLOR][PIXEL_SHADE_BRIGHT]);
	}
	else
	{
		j += BMXored.LoadBitmap(PixelColorIDs[NORMAL_XORED_COLOR][PIXEL_SHADE_BRIGHT]);
	}


	if (i == NORMAL_SKIPPED_COLOR)
	{
		j += BMSkipped.LoadBitmap(PixelColorIDs[ALTERNATE_SKIPPED_COLOR][PIXEL_SHADE_DIM]);
	}
	else
	{
		j += BMSkipped.LoadBitmap(PixelColorIDs[NORMAL_SKIPPED_COLOR][PIXEL_SHADE_DIM]);
	}
	j += BMDim.LoadBitmap(PixelColorIDs[i][PIXEL_SHADE_DIM]);
	j += BMMedium.LoadBitmap(PixelColorIDs[i][PIXEL_SHADE_MEDIUM]);
	j += BMBright.LoadBitmap(PixelColorIDs[i][PIXEL_SHADE_BRIGHT]);

	if (j != 6)
	{
		AfxMessageBox("Problem loading pixel bitmaps.");
		return;
	}
	j = 0;
	CBitmap *old_hOff = hOff.SelectObject(&BMOff);
	if (old_hOff)
	{
		j++;
	}
	CBitmap *old_hXored = hXored.SelectObject(&BMXored);
	if (old_hXored)
	{
		j++;
	}
	CBitmap *old_hSkipped = hSkipped.SelectObject(&BMSkipped);
	if (old_hSkipped)
	{
		j++;
	}
	CBitmap *old_hDim = hDim.SelectObject(&BMDim);
	if (old_hDim)
	{
		j++;
	}
	CBitmap *old_hMedium = hMedium.SelectObject(&BMMedium);
	if (old_hMedium)
	{
		j++;
	}
	CBitmap *old_hBright = hBright.SelectObject(&BMBright);
	if (old_hBright)
	{
		j++;
	}

	if (j != 6)
	{
		AfxMessageBox("Problem loading pixel bitmap objects.");
		return;
	}

	for (i = 0; i < DMD_ROWS; i++)
	{
		for (j = 0; j < (DMD_COLUMNS/8); j++)
		{
			for (ReadMask = 0x01, k = 0; k < 8; k++,ReadMask <<= 1)
			{
				PLANE_BITS = 0x00;
				if (*Plane_0Ptr & ReadMask)
				{
					PLANE_BITS |= PLANE0_ON;
				}
				if (*Plane_0Skipped & ReadMask)
				{
					PLANE_BITS |= PLANE0_SKIPPED;
				}
				if (*Plane_0XorFlags & ReadMask)
				{
                    if (*Plane_0XorBits & ReadMask)
                    {
					   PLANE_BITS |= PLANE0_XORED; // XOR flag <and> XOR bit then flip bit from previous display
                    }
                    else
                    {
                       PLANE_BITS |= PLANE0_SKIPPED; // XOR flag <and NOT> XOR bit, then treat it as a skip
                    }
				}
				if (*Plane_1Ptr & ReadMask)
				{
					PLANE_BITS |= PLANE1_ON;
				}
				if (*Plane_1Skipped & ReadMask)
				{
					PLANE_BITS |= PLANE1_SKIPPED;
				}
				if (*Plane_1XorFlags & ReadMask)
				{
                    if (*Plane_1XorBits & ReadMask)
                    {
					   PLANE_BITS |= PLANE1_XORED; // XOR flag <and> XOR bit then flip bit from previous display
                    }
                    else
                    {
                       PLANE_BITS |= PLANE1_SKIPPED; // XOR flag <and NOT> XOR bit, then treat it as a skip
                    }
				}

                // Quick check if we have any xor or skipped pixels
                if ((PLANE_BITS & (PLANE0_SKIPPED | PLANE1_SKIPPED)) && !SkippedCheck)
                {
                    bAnySkippedPixel = TRUE;
                }
                if ((PLANE_BITS & (PLANE0_XORED | PLANE1_XORED)) && !XoredCheck)
                {
                    bAnyXoredPixel = TRUE;
                }

				//
				ColumnIndex = ((((j * 8) + k)) * PIXEL_WIDTH);
				RowIndex = (i * PIXEL_HEIGHT);

				//
				// Determine what color to show for medium colored plane
				//
				if (PaneMask & DMD_FULLFRAME_PAINT_DIM)
				{
                    thisPixel0 = ThisPixel_Off;
					if (PLANE_BITS & PLANE0_ON)
					{
                       thisPixel0 = ThisPixel_On;
					}
					else if (PLANE_BITS & PLANE0_SKIPPED)
					{
						if (SkippedCheck)
						{
                           thisPixel0 = ThisPixel_Skipped;
						}
						else if (*Plane_0Previous & ReadMask)
                        {
                           thisPixel0 = ThisPixel_On;
						}
					}
					else if (PLANE_BITS & PLANE0_XORED)
					{
						if (XoredCheck)
						{
                           thisPixel0 = ThisPixel_Xored;
						}
						else if (!(*Plane_0Previous & ReadMask))
                        {
                           thisPixel0 = ThisPixel_On;
						}
					}
                    switch (thisPixel0)
                    {
                       case ThisPixel_Off:
                          pDc->BitBlt(ColumnIndex,RowIndex,PIXEL_WIDTH,PIXEL_HEIGHT,&hOff,0,0,SRCCOPY);
                          cbPixel0 = '0'; // pixel off
                          break;
                       case ThisPixel_On:
                          pDc->BitBlt(ColumnIndex,RowIndex,PIXEL_WIDTH,PIXEL_HEIGHT,&hMedium,0,0,SRCCOPY);
                          cbPixel0 = '2'; // medium pixel on
                          break;
                       case ThisPixel_Xored:
                          pDc->BitBlt(ColumnIndex,RowIndex,PIXEL_WIDTH,PIXEL_HEIGHT,&hXored,0,0,SRCCOPY);
                          cbPixel0 = 'x'; // xored pixel, user has XOR checkbox checked
                          break;
                       case ThisPixel_Skipped:
                          pDc->BitBlt(ColumnIndex,RowIndex,PIXEL_WIDTH,PIXEL_HEIGHT,&hSkipped,0,0,SRCCOPY);
                          cbPixel0 = '_'; // skipped pixel, user has SKIPPED checkbox checked
                          break;
                       default:
                          break;
                    }
				}
				
				RowIndex += ((DMD_ROWS + 1) * PIXEL_HEIGHT);

				//
				// Determine what color to show for dim plane
				//
				if (PaneMask & DMD_FULLFRAME_PAINT_MEDIUM)
				{
                    thisPixel1 = ThisPixel_Off;
					if (PLANE_BITS & PLANE1_ON)
					{
                       thisPixel1 = ThisPixel_On;
					}
					else if (PLANE_BITS & PLANE1_SKIPPED)
					{
						if (SkippedCheck)
						{
                           thisPixel1 = ThisPixel_Skipped;
						}
						else if (*Plane_1Previous & ReadMask)
						{
                           thisPixel1 = ThisPixel_On;
						}
					}
					else if (PLANE_BITS & PLANE1_XORED)
					{
						if (XoredCheck)
						{
                           thisPixel1 = ThisPixel_Xored;
						}
						else if (!(*Plane_1Previous & ReadMask))
						{
                           thisPixel1 = ThisPixel_On;
						}
					}
                    switch (thisPixel1)
                    {
                       case ThisPixel_Off:
                          pDc->BitBlt(ColumnIndex,RowIndex,PIXEL_WIDTH,PIXEL_HEIGHT,&hOff,0,0,SRCCOPY);
                          cbPixel1 = '0'; // pixel off
                          break;
                       case ThisPixel_On:
                          pDc->BitBlt(ColumnIndex,RowIndex,PIXEL_WIDTH,PIXEL_HEIGHT,&hDim,0,0,SRCCOPY);
                          cbPixel1 = '1'; // dim pixel on
                          break;
                       case ThisPixel_Xored:
                          pDc->BitBlt(ColumnIndex,RowIndex,PIXEL_WIDTH,PIXEL_HEIGHT,&hXored,0,0,SRCCOPY);
                          cbPixel1 = 'x'; // xored pixel, user has XOR checkbox checked
                          break;
                       case ThisPixel_Skipped:
                          pDc->BitBlt(ColumnIndex,RowIndex,PIXEL_WIDTH,PIXEL_HEIGHT,&hSkipped,0,0,SRCCOPY);
                          cbPixel1 = '_'; // skipped pixel, user has SKIPPED checkbox checked
                          break;
                       default:
                          break;
                    }
				}

                // Save "previous" frame data
                if (thisPixel0 == ThisPixel_Off)
                {
                   *Plane_0Previous &= ~ReadMask;
                }
                else if (thisPixel0 == ThisPixel_On)
                {
                   *Plane_0Previous |= ReadMask;
                }

                if (thisPixel1 == ThisPixel_Off)
                {
                   *Plane_1Previous &= ~ReadMask;
                }
                else if (thisPixel1 == ThisPixel_On)
                {
                   *Plane_1Previous |= ReadMask;
                }

				RowIndex += ((DMD_ROWS + 1) * PIXEL_HEIGHT);

				//
				// Determine what color to show for blended plane
				//
				if (PaneMask & DMD_FULLFRAME_PAINT_BLENDED)
				{
                   if ((thisPixel0 == ThisPixel_On) && (thisPixel1 == ThisPixel_On))
                   {
                      pDc->BitBlt(ColumnIndex,RowIndex,PIXEL_WIDTH,PIXEL_HEIGHT,&hBright,0,0,SRCCOPY);
                      cbPixel2 = '3'; // pixel bright
                   }
                   else if (thisPixel0 == ThisPixel_On)
                   {
                      pDc->BitBlt(ColumnIndex,RowIndex,PIXEL_WIDTH,PIXEL_HEIGHT,&hMedium,0,0,SRCCOPY);
                      cbPixel2 = '2'; // pixel medium
                   }
                   else if (thisPixel1 == ThisPixel_On)
                   {
                      pDc->BitBlt(ColumnIndex,RowIndex,PIXEL_WIDTH,PIXEL_HEIGHT,&hDim,0,0,SRCCOPY);
                      cbPixel2 = '1'; // pixel dim
                   }
                   else
                   {
                      pDc->BitBlt(ColumnIndex,RowIndex,PIXEL_WIDTH,PIXEL_HEIGHT,&hOff,0,0,SRCCOPY);
                      cbPixel2 = '0'; // pixel off
                   }
				}

                // if clipboard operation is in use, push the cbPixel to clipboard ram
                if (cbPtr != NULL)
                {
                   switch (selectedTitleBox)
                   {
                      case 1:
                          *cbPtr++ = cbPixel0;
                          break;
                      case 2:
                          *cbPtr++ = cbPixel1;
                          break;
                      case 3:
                          *cbPtr++ = cbPixel2;
                          break;
                      default:
                          break;
                    }
                }
			}
			Plane_0Ptr++;
			Plane_1Ptr++;
			Plane_0Skipped++;
			Plane_1Skipped++;
			Plane_0XorFlags++;
			Plane_1XorFlags++;
			Plane_0XorBits++;
			Plane_1XorBits++;
            Plane_0Previous++;
            Plane_1Previous++;
		}
        // Add newline for clipboard operation
        if (cbPtr != NULL)
        {
           *cbPtr++ = '\r';
           *cbPtr++ = '\n';
        }
	}
    // Add trailing null for clipboard operations
    if (cbPtr != NULL)
    {
       *cbPtr++ = NULL;
    }

	hOff.SelectObject(old_hOff);
	hXored.SelectObject(old_hXored);
	hSkipped.SelectObject(old_hSkipped);
	hDim.SelectObject(old_hDim);
	hMedium.SelectObject(old_hMedium);
	hBright.SelectObject(old_hBright);

    // Finish up clipboard operation
    if ((cbData != NULL) && (::SetClipboardData( CF_TEXT, cbData ) != NULL ))
    {
        // ...  
        CloseClipboard();
    }

    // We know the "Previous" data has been filled in, so make sure the Wipe button is enabled
	m_Wipe.EnableWindow((((bAnySkippedPixel == TRUE) || (bAnyXoredPixel == TRUE)) && (bWiped != TRUE)) ? TRUE : FALSE);
}

void DMD::OnPaint() 
{
	CPaintDC dc(this); // device context for painting

	switch (dialogType)
	{
		case DMD_DIALOG_TYPE_GRAPHICS:
			UpdateCheckboxText();
			PaintDMDPanelImage(&dc, &FullFrameImageData.Planes, DMD_FULLFRAME_PAINT_DIM | DMD_FULLFRAME_PAINT_MEDIUM | DMD_FULLFRAME_PAINT_BLENDED);
			break;

		case DMD_DIALOG_TYPE_FONTDATA:
		case DMD_DIALOG_TYPE_ANIDATA:
			// Paint image data Panes 1 & 2, Paint blended image pane only if Plane1 status is valid
			PaintDMDPanelImage(&dc, &VariableSizedImageData.Planes, DMD_FULLFRAME_PAINT_DIM | DMD_FULLFRAME_PAINT_MEDIUM | (VariableSizedImageData.Planes.Plane1.Plane_Status==PLANE_STATUS_VALID? DMD_FULLFRAME_PAINT_BLENDED:0));
			// Paint Pane 3 with the single bi-colored graphic image we loaded at init only if VariableSizedImageData Plane1 is invalid
			if (VariableSizedImageData.Planes.Plane1.Plane_Status != PLANE_STATUS_VALID)
			{
				PaintDMDPanelImage(&dc, &FullFrameImageData.Planes, DMD_FULLFRAME_PAINT_BLENDED);
			}
			break;

		default:
			break;
	}
}

int DMD::PreAnalyzeVariableSizedImageTable()
{
	LPTSTR Ptr;
	unsigned long Addr;
	int TableCount = 0;

	// Standard validations and sanity checks
	if (!VariableSizedImageData.TableAddress)
	{
		TmpStr.Format("Unexpected NULL VariableSizedImageData.TableAddress");
		DebugControlKeyMsgStrPrint(TmpStr);
	}
	if (VariableSizedImageData.TableAddress >= CommonData.ROMSize)
	{
		TmpStr.Format("Unexpected table address 0x%x is >= ROMSize 0x%x",VariableSizedImageData.TableAddress,CommonData.ROMSize);
		DebugControlKeyMsgStrPrint(TmpStr);
	}

	Ptr = &CommonData.StartPtr[VariableSizedImageData.TableAddress];

	// We're now at the start of the table, lets count up the number table entries
	while (GetROMAddressFromAddrOf3ByteWPCAddrPage(Ptr,&Addr) == 0)
	{
		VariableSizedImageData.maxTableIndex++;
		if (GetLastImageIndex(NULL, (VariableSizedImageData.maxTableIndex-1)) != 0)
		{
			VariableSizedImageData.maxTableIndex--;
			TmpStr.Format("Stopped looking for image tables due to GetLastImageIndex() error on TableIndex %d",VariableSizedImageData.maxTableIndex);
			DebugControlKeyMsgStrPrint(TmpStr);
			break;
		}
		Ptr += 3;
		TableCount++;
	}

	//TmpStr.Format("Determined TableCount: %d",TableCount);
	//DebugControlKeyMsgStrPrint(TmpStr);

	if (TableCount == 0)
	{
		TmpStr.Format("Found 0 table entries");
		AfxMessageBox(TmpStr);
		return -1;
	}

	// Last 0-based, valid, image table index
	VariableSizedImageData.minTableIndex = 0;
	VariableSizedImageData.maxTableIndex = (TableCount - 1);

	// Backup to the last valid image table, for purposes of debug message/validation
	//TmpStr.Format("Last Table: 0x%02x 0x%02x 0x%02x, ROM Addr 0x%x",(*(Ptr-3))&0xFF,(*((Ptr-2)))&0xFF,(*((Ptr-1)))&0xFF,Addr);
	//DebugControlKeyMsgStrPrint(TmpStr);

	//
	if (GetLastImageIndex(&VariableSizedImageData.maxImageIndex, VariableSizedImageData.maxTableIndex) != 0)
	{
		TmpStr.Format("Error looking up max image index for last table index %d\n",VariableSizedImageData.maxTableIndex);
		AfxMessageBox(TmpStr);
		return -1;
	}

	//
	if (GetFirstImageIndex(&VariableSizedImageData.minImageIndex, VariableSizedImageData.minTableIndex) != 0)
	{
		TmpStr.Format("Error looking up min image index for first table index %d\n",VariableSizedImageData.maxTableIndex);
		AfxMessageBox(TmpStr);
		return -1;
	}

	//
	//TmpStr.Format("Determined maxTableIndex %d, maxImageIndex 0x%02x",VariableSizedImageData.maxTableIndex,(VariableSizedImageData.maxImageIndex&0xFF));
	//DebugControlKeyMsgStrPrint(TmpStr);

	return 0;
}

int DMD::GetFirstImageIndex(int *pImageIndex, int TableIndex)
{
	int ImageIndex = 0;

	if (GetNextImageIndex(&ImageIndex, TableIndex) != 0)
	{
		return -1;
	}

	if (pImageIndex != NULL)
	{
		*pImageIndex = ImageIndex;
	}

	return 0;
}

int DMD::GetLastImageIndex(int *pImageIndex, int TableIndex)
{
	int ImageIndex = 0;
	int hit = 0;

	while (GetNextImageIndex(&ImageIndex, TableIndex) == 0)
	{
		hit = 1;
	}

	if (hit == 0) 
	{
		return -1;
	}

	if (pImageIndex != NULL)
	{
		*pImageIndex = ImageIndex;
	}

	return 0;
}

int DMD::GetPrevImageIndex(int *pImageIndex, int TableIndex)
{
	unsigned long Addr;
	LPTSTR Ptr;
	unsigned char ImageIndexMin;
	unsigned char ImageIndexMax;
	int windUp;

	// Standard validations and sanity checks
	if (!VariableSizedImageData.TableAddress)
	{
		return -1;
	}
	if (VariableSizedImageData.TableAddress >= CommonData.ROMSize)
	{
		return -1;
	}
	if ((TableIndex < VariableSizedImageData.minTableIndex) || (TableIndex > VariableSizedImageData.maxTableIndex))
	{
		return -1;
	}
	if (pImageIndex == NULL)
	{
		return -1;
	}

	if (GetROMAddressOfVariableSizedImageTable(&Addr, TableIndex) != 0)
	{
		return -1;
	}

	// Get pointer to area in ROM of actual table
	Ptr = &CommonData.StartPtr[Addr];
    // Need to start at last min/max pair and work down
	windUp = 0;
	while (((*Ptr) & 0xFF) != 0x00)
	{
		Ptr += 2;  // walk past the min/max pair
		windUp++;
	}

	// Now reverse back through the min/max pairs...
	while (windUp != 0)
	{
		Ptr -= 2;
		windUp--;

		ImageIndexMin = (*Ptr)&0xFF;
		ImageIndexMax = (*(Ptr+1))&0xFF;

		//
		if (ImageIndexMin > ImageIndexMax)
		{
			return -1;
		}
		if (((*pImageIndex)&0xFF) > (ImageIndexMax&0xFF))
		{
			*pImageIndex = ImageIndexMax;
			return 0;
		}
		if (((*pImageIndex)&0xFF) > (ImageIndexMin&0xFF))
		{
			*pImageIndex = (*pImageIndex)-1;
			return 0;
		}
	}
	return -1;
}

int DMD::GetNextImageIndex(int *pImageIndex, int TableIndex)
{
	unsigned long Addr;
	LPTSTR Ptr;
	unsigned char ImageIndexMin;
	unsigned char ImageIndexMax;

	// Standard validations and sanity checks
	if (!VariableSizedImageData.TableAddress)
	{
		return -1;
	}
	if (VariableSizedImageData.TableAddress >= CommonData.ROMSize)
	{
		return -1;
	}
	if ((TableIndex < VariableSizedImageData.minTableIndex) || (TableIndex > VariableSizedImageData.maxTableIndex))
	{
		return -1;
	}
	if (pImageIndex == NULL)
	{
		return -1;
	}

	if (GetROMAddressOfVariableSizedImageTable(&Addr, TableIndex) != 0)
	{
		return -1;
	}

	// Get pointer to area in ROM of actual table
	Ptr = &CommonData.StartPtr[Addr];

	while (((*Ptr) & 0xFF) != 0x00)
	{
		ImageIndexMin = (*Ptr++)&0xFF;
		ImageIndexMax = (*Ptr++)&0xFF;

		//
		if (ImageIndexMin > ImageIndexMax)
		{
			return -1;
		}
		if (((*pImageIndex)&0xFF) < (ImageIndexMin&0xFF))
		{
			*pImageIndex = ImageIndexMin;
			return 0;
		}
		if (((*pImageIndex)&0xFF) < (ImageIndexMax&0xFF))
		{
			*pImageIndex = (*pImageIndex)+1;
			return 0;
		}
	}
	return -1;
}

int DMD::GetAddrToWPCAddressOfVariableSizedImageTable(unsigned long *pAddr, int TableIndex)
{
	unsigned long romAddr;

	// Standard validations and sanity checks
	if (!VariableSizedImageData.TableAddress)
	{
		return -1;
	}
	if (VariableSizedImageData.TableAddress >= CommonData.ROMSize)
	{
		return -1;
	}
	if ((TableIndex < VariableSizedImageData.minTableIndex) || (TableIndex > VariableSizedImageData.maxTableIndex))
	{
		return -1;
	}

	romAddr = VariableSizedImageData.TableAddress + (3 * TableIndex);

	if (romAddr >= CommonData.ROMSize)
	{
		return -1;
	}

	if (pAddr != NULL)
	{
		*pAddr = romAddr;
	}
	
	return 0;
}

int DMD::ExtractWPCAddrAndPageOfImageTable(int *pAddr, int *pPage, int TableIndex)
{
	unsigned long romAddr;
	LPTSTR Ptr;
	int Addr;
	int Page;

	// Standard validations and sanity checks
	if (!VariableSizedImageData.TableAddress)
	{
		return -1;
	}
	if (VariableSizedImageData.TableAddress >= CommonData.ROMSize)
	{
		return -1;
	}
	if ((TableIndex < VariableSizedImageData.minTableIndex) || (TableIndex > VariableSizedImageData.maxTableIndex))
	{
		return -1;
	}

	if (GetAddrToWPCAddressOfVariableSizedImageTable(&romAddr, TableIndex) != 0)
	{
		return -1;
	}

	Ptr = &CommonData.StartPtr[romAddr];

	Addr = (*(Ptr)) & 0xFF;
	Addr <<= 8;
	Addr |= (*(Ptr+1)) & 0xFF;
	Addr &= 0xFFFF;
	Page = (*(Ptr+2)) & 0xFF;

	{
		// Some ROMs have another pointer that needs de-referenced.  Instead of pointing to
		// the image table, its an address to the table within the same bank.  It appears
		// 0x00 follows the 2-byte address.
		int TempAddr;
		int TempPage;
		if (GetROMAddressFromWPCAddrAndPage(&romAddr, Addr, Page) != 0)
		{
			return -1;
		}
		Ptr = &CommonData.StartPtr[romAddr];

		TempAddr = (*(Ptr)) & 0xFF;
		TempAddr <<= 8;
		TempAddr |= (*(Ptr+1)) & 0xFF;
		TempAddr &= 0xFFFF;
		TempPage = (*(Ptr+2)) & 0xFF;

		TmpStr.Format("Testing Tempaddr 0x%04x and Page 0x%02x",TempAddr,TempPage);
		DebugShiftKeyMsgStrPrint(TmpStr);

		if (((TempAddr >= BASE_CODE_ADDR_PAGED_ROM) && (TempAddr < (BASE_CODE_ADDR_PAGED_ROM + PAGE_LENGTH))) 
			/*&& (TempPage == 0x00)*/)
		{
			Addr = TempAddr;
		}
		TmpStr.Format("ExtractWPCAddrAndPageOfImageTable() FIXUP, Addr fixed to $%04x,%02x",Addr,Page);
		DebugShiftKeyMsgStrPrint(TmpStr);
	}

	if (pAddr != NULL)
	{
		*pAddr = Addr;
	}
	if (pPage != NULL)
	{
		*pPage = Page;
	}
	return 0;
}


int DMD::GetROMAddressOfVariableSizedImageTable(unsigned long *pRomAddr, int TableIndex)
{
	int Addr;
	int Page;

	if (ExtractWPCAddrAndPageOfImageTable(&Addr, &Page, TableIndex) != 0)
	{
		return -1;
	}

	if (GetROMAddressFromWPCAddrAndPage(pRomAddr, Addr, Page) != 0)
	{
		return -1;
	}

	return 0;
}

int DMD::GetVariableSizedImageTableMetadata(int TableIndex, int *pTableHeight, int *pTableSpacing)
{
	unsigned long Addr;
	LPTSTR Ptr;
	int TableHeight;
	int TableSpacing;  // not sure at this point, 0x01 follows TableHeight

	if (GetROMAddressOfVariableSizedImageTable(&Addr, TableIndex) != 0)
	{
		return -1;
	}

	// sanity check (maybe a bit redundant at this point)
	if (Addr >= CommonData.ROMSize)
	{
		return -1;
	}

	// Get pointer to area in ROM of actual table
	Ptr = &CommonData.StartPtr[Addr];

	// Past the 0x00
	while (((*Ptr++) & 0xFF) != 0x00);

	TableHeight = *Ptr++;
	TableSpacing = *Ptr++;

	if (pTableHeight != NULL)
	{
		*pTableHeight = TableHeight;
	}
	if (pTableSpacing != NULL)
	{
		*pTableSpacing = TableSpacing;
	}

	return 0;
}

int DMD::GetROMAddressOfVariableSizedImageIndex(unsigned long *pRomAddr, int TableIndex, int ImageIndex)
{
	unsigned long Addr;
	int Page;
	LPTSTR Ptr;
	int TableHeight;
	int TableSpacing;  // not sure at this point, 0x01 follows TableHeight
	int ImageIndexMin, ImageIndexMax, ImageNum, ImageFound;

	//TmpStr.Format("GetROMAddressOfVariableSizedImageIndex() Looking up ROM addres for TableIndex %d, ImageIndex 0x%02x",TableIndex,ImageIndex);
	//DebugControlKeyMsgStrPrint(TmpStr);

	if (GetROMAddressOfVariableSizedImageTable(&Addr, TableIndex) != 0)
	{
		return -1;
	}

	// sanity check (maybe a bit redundant at this point)
	if (Addr >= CommonData.ROMSize)
	{
		return -1;
	}

	// Get pointer to area in ROM of actual table
	Ptr = &CommonData.StartPtr[Addr];
	ImageNum = ImageFound = 0;

	// Figure out which Nth image number this is in the table, there are min/max groups which cause gaps which we account for here
	while (((*Ptr) & 0xFF) != 0x00)
	{
		ImageIndexMin = (*Ptr++)&0xFF;
		ImageIndexMax = (*Ptr++)&0xFF;

		//TmpStr.Format("GetROMAddressOfVariableSizedImageIndex() ImageIndexMin %d ImageIndexMax %d",ImageIndexMin,ImageIndexMax);
		//DebugControlKeyMsgStrPrint(TmpStr);

		//
		if (ImageIndexMin > ImageIndexMax)
		{
			return -1;
		}
		if (ImageFound == 0)
		{
			while (ImageIndexMin <= ImageIndexMax)
			{
				if (ImageIndex <= ImageIndexMin)
				{
					//TmpStr.Format("GetROMAddressOfVariableSizedImageIndex() ImageFound, ImageNum %d, ImageIndexMin %d, ImageIndexMax %d",ImageNum,ImageIndexMin,ImageIndexMax);
					//DebugControlKeyMsgStrPrint(TmpStr);

					ImageFound = 1;
					break;
				}
				ImageNum++;
				ImageIndexMin++;
			}
		}
	}

	//
	Ptr++; // get past the 0x00 byte
	TableHeight = *Ptr++;
	TableSpacing = *Ptr++;

	//
	//TmpStr.Format("GetROMAddressOfVariableSizedImageIndex() TableHeight %d, TableSpacing %d",TableHeight,TableSpacing);
	//DebugControlKeyMsgStrPrint(TmpStr);

	// advance to desired image
	Ptr += (ImageNum * 2);

	// Addr comes from pointer in table
	Addr = (*(Ptr)) & 0xFF;
	Addr <<= 8;
	Addr |= (*(Ptr+1)) & 0xFF;
	Addr &= 0xFFFF;

	// Page is looked up from the current table index
	if (ExtractWPCAddrAndPageOfImageTable(NULL, &Page, TableIndex) != 0)
	{
		return -1;
	}

	if (GetROMAddressFromWPCAddrAndPage(&Addr, Addr, Page) != 0)
	{
		return -1;
	}

	//
	//TmpStr.Format("GetROMAddressOfVariableSizedImageIndex() TableHeight %d, TableSpacing %d ImageIndex 0x%02x at 0x%05x",TableHeight,TableSpacing,ImageIndex,Addr);
	//DebugControlKeyMsgStrPrint(TmpStr);

	if (pRomAddr != NULL)
	{
		*pRomAddr = Addr;
	}
	return 0;
}

int DMD::GetROMAddressFromWPCAddrAndPage(unsigned long *pRomAddr, unsigned long Addr, unsigned char Page)
{
	// In  : The raw 16-bit address and 8-bit page from the WPC 3-byte address
	// Out : The 32-bit address in the ROM image corresponding to the WPC Addr and Page

	unsigned long romAddr;

	if ((Addr >= BASE_CODE_ADDR_NONPAGED_ROM) && (Addr < (BASE_CODE_ADDR_NONPAGED_ROM + NONPAGED_LENGTH)))
	{
		if (Page != NONPAGED_BANK_INDICATOR)
		{
			TmpStr.Format("GetROMAddressFromWPCAddrAndPage() Non-banked WPC addr 0x%04x followed by page byte 0x%02x, normal when reading from opcode or some ROMs with 2-byte table addr entries. Forcing page to 0x%02x",Addr,Page,NONPAGED_BANK_INDICATOR);
			DebugShiftKeyMsgStrPrint(TmpStr);
			Page = NONPAGED_BANK_INDICATOR;
		}
	}

	if ((Page == NONPAGED_BANK_INDICATOR) && 
		(Addr >= BASE_CODE_ADDR_NONPAGED_ROM) &&
		(Addr < (BASE_CODE_ADDR_NONPAGED_ROM+NONPAGED_LENGTH)))
	{
		romAddr = ((CommonData.TotalPages-2) * PAGE_LENGTH) + (Addr - BASE_CODE_ADDR_NONPAGED_ROM);
	}
	else if ((Page >= CommonData.BasePageIndex) &&
			 (Page < (CommonData.BasePageIndex+CommonData.TotalPages-2)) &&
			 (Addr >= BASE_CODE_ADDR_PAGED_ROM) &&
			 (Addr < BASE_CODE_ADDR_NONPAGED_ROM))
	{
		romAddr = ((Page-CommonData.BasePageIndex) * PAGE_LENGTH) + (Addr - BASE_CODE_ADDR_PAGED_ROM);
	}
	else
	{
		TmpStr.Format("Invalid WPC Addr and Page, $%04x,%02x, BasePage 0x%02x, TotalPages 0x%02x",
			          Addr,Page,CommonData.BasePageIndex,CommonData.TotalPages);
		DebugShiftKeyMsgStrPrint(TmpStr);
		return -1;
	}
	if (romAddr >= CommonData.ROMSize)
	{
		TmpStr.Format("Unexpected: Calculated addr in ROM 0x%x is greater than determined ROM size 0x%x",romAddr,CommonData.ROMSize);
		DebugShiftKeyMsgStrPrint(TmpStr);
		return -1;
	}

	if (pRomAddr != NULL)
	{
		*pRomAddr = romAddr;
	}
	return 0;
}

int DMD::ExtractWPCAddrAndPageFromBuffer(LPTSTR pSrc, unsigned long *pDstAddr, unsigned char *pDstPage)
{
	// In  : Address of memory containg a 3-byte WPC Address notation
	// Out : The raw 16-bit address and 8-bit page from the WPC 3-byte address

	unsigned long Addr;
	unsigned char Page;

	Addr = (*(pSrc)) & 0xFF;
	Addr <<= 8;
	Addr |= (*(pSrc+1)) & 0xFF;
	Addr &= 0xFFFF;
	Page = (*(pSrc+2)) & 0xFF;

	if ((Addr >= BASE_CODE_ADDR_NONPAGED_ROM) && (Addr < (BASE_CODE_ADDR_NONPAGED_ROM + NONPAGED_LENGTH)))
	{
		if (Page != NONPAGED_BANK_INDICATOR)
		{
			TmpStr.Format("ExtractWPCAddrAndPageFromBuffer() Non-banked WPC addr 0x%04x followed by page byte 0x%02x, normal when reading from opcode or some ROMs with 2-byte table addr entries. Forcing page to 0x%02x",Addr,Page,NONPAGED_BANK_INDICATOR);
			DebugShiftKeyMsgStrPrint(TmpStr);
			Page = NONPAGED_BANK_INDICATOR;
		}
	}

	if (pDstAddr != NULL)
	{
		// Caller wants addr, validate it makes sense first
		if (((Addr >= BASE_CODE_ADDR_PAGED_ROM) && (Addr < (BASE_CODE_ADDR_PAGED_ROM + PAGE_LENGTH))) ||
			((Addr >= BASE_CODE_ADDR_NONPAGED_ROM) && (Addr < (BASE_CODE_ADDR_NONPAGED_ROM + NONPAGED_LENGTH))))
		{
			*pDstAddr = Addr;
		}
		else
		{
			TmpStr.Format("Expected a WPC Addr, but read 0x%04x",Addr);
			DebugShiftKeyMsgStrPrint(TmpStr);
			return -1;
		}
	}
	if (pDstPage != NULL)
	{
		// Caller wants page, validate it makes sense first
		if (((Page >= CommonData.BasePageIndex) && (Page < (CommonData.BasePageIndex+CommonData.TotalPages))) ||
			(Page == NONPAGED_BANK_INDICATOR))
		{
			*pDstPage = Page;
		}
		else
		{
			TmpStr.Format("Expected a WPC Page Number, but read 0x%02x, Base is 0x%02x, Total Pages 0x%02x",Page,CommonData.BasePageIndex,CommonData.TotalPages);
			DebugShiftKeyMsgStrPrint(TmpStr);
			return -1;
		}
	}
	return 0;
}

int DMD::GetROMAddressFromAddrOf3ByteWPCAddrPage(LPTSTR pSrc, unsigned long *pDst)
{
	// In  : Address of memory containg a 3-byte WPC Address notation
	// Out : Address in ROM image to which the WPC 3-byte address refers

	unsigned long Addr;
	unsigned char Page;

	if (ExtractWPCAddrAndPageFromBuffer(pSrc, &Addr, &Page) != 0)
	{
		TmpStr.Format("Error from ExtractWPCAddrAndPageFromBuffer(), Passed it ptr to: 0x%02x 0x%02x 0x%02x",(*pSrc)&0xFF,(*(pSrc+1))&0xFF,(*(pSrc+2))&0xFF);
		DebugShiftKeyMsgStrPrint(TmpStr);
		return -1;
	}

	TmpStr.Format("GetROMAddressFromAddrOf3ByteWPCAddrPage() WPC TableAddress $%04x,%02x",Addr,Page);
	DebugShiftKeyMsgStrPrint(TmpStr);

	if (GetROMAddressFromWPCAddrAndPage(&Addr, Addr, Page) != 0)
	{
		TmpStr.Format("Error from GetROMAddressFromWPCAddrAndPage(), Passed it WPC Addr $%04x,%02x",Addr,Page);
		DebugShiftKeyMsgStrPrint(TmpStr);
		return -1;
	}

	TmpStr.Format("GetROMAddressFromAddrOf3ByteWPCAddrPage() ROM TableAddress 0x%x",Addr);
	DebugShiftKeyMsgStrPrint(TmpStr);

	if (pDst != NULL)
	{
		*pDst = Addr;
	}

	return 0;
}

int DMD::ProcessHitType(int HitType, LPTSTR HitTablePtr, LPTSTR HitPagePtr, LPTSTR Ptr, unsigned long *pTbl)
{
	unsigned long Addr;
	char HitBuf[3];

	switch (HitType)
	{
		// this not used at this time...
		case HITTYPE_TBL_ADDR_ADDR_ADDR :
			//
			TmpStr.Format("Potential Match. HitType 0x%02x, HitBytes 0x%02x 0x%02x",(*(Ptr-1))&0xFF,(*HitTablePtr)&0xFF,(*(HitTablePtr+1))&0xFF);
			DebugShiftKeyMsgStrPrint(TmpStr);

			//
			if (GetROMAddressFromAddrOf3ByteWPCAddrPage(HitTablePtr, &Addr) != 0)
			{
				TmpStr.Format("Error from GetROMAddressFromAddrOf3ByteWPCAddrPage(), Passed it WPC Ptr to $%02x %02x",(*HitTablePtr)&0xFF,(*(HitTablePtr+1))&0xFF);
				DebugShiftKeyMsgStrPrint(TmpStr);
				return -1;
			}

			//
			TmpStr.Format("HITTYPE_TBL_ADDR_ADDR_ADDR derived ROM TableAddressAddress 0x%04x, going to HITTYPE_TBL_ADDR_ADDR",Addr);
			DebugShiftKeyMsgStrPrint(TmpStr);

			HitTablePtr = &CommonData.StartPtr[Addr];
			// no break!  now that we have the table address address, go to the following to get WPC address of the table, and then ROM address of the table

		case HITTYPE_TBL_ADDR_ADDR :
			//
			TmpStr.Format("Potential Match. HitType 0x%02x, HitBytes 0x%02x 0x%02x",(*(Ptr-1))&0xFF,(*HitTablePtr)&0xFF,(*(HitTablePtr+1))&0xFF);
			DebugShiftKeyMsgStrPrint(TmpStr);
			//
			if (GetROMAddressFromAddrOf3ByteWPCAddrPage(HitTablePtr, &Addr) != 0)
			{
				TmpStr.Format("Error from GetROMAddressFromAddrOf3ByteWPCAddrPage(), Passed it WPC Ptr to $%02x %02x",(*HitTablePtr)&0xFF,(*(HitTablePtr+1))&0xFF);
				DebugShiftKeyMsgStrPrint(TmpStr);
				return -1;
			}

			//
			TmpStr.Format("HITTYPE_TBL_ADDR_ADDR derived TableAddress of 0x%04x, going to HITTYPE_TBL_ADDR",Addr);
			DebugShiftKeyMsgStrPrint(TmpStr);

			HitTablePtr = &CommonData.StartPtr[Addr];
			HitPagePtr = &CommonData.StartPtr[Addr+2]; // in some cases when addr is in non-banked ROM this byte will get ignored
			// no break!  now that we have the WPC table address, go to the following to get ROM address from WPC address

		case HITTYPE_TBL_ADDR:
			//
			if (HitTablePtr == NULL)
			{
				TmpStr.Format("HITTYPE_TBL_ADDR, but HitTablePtr is NULL");
				DebugShiftKeyMsgStrPrint(TmpStr);
				return -1;
			}
			//
			HitBuf[0] = (*HitTablePtr)&0xFF;
			HitBuf[1] = (*(HitTablePtr+1))&0xFF;

			if (HitPagePtr == NULL)
			{
				// Null HitPagePtr is okay if the address is in non-paged ROM
				unsigned long Addr;

				Addr = (HitBuf[0] & 0xFF);
				Addr <<= 8;
				Addr |= (HitBuf[1] & 0xFF);
				Addr &= 0xFFFF;

				if (!((Addr >= BASE_CODE_ADDR_NONPAGED_ROM) && (Addr < (BASE_CODE_ADDR_NONPAGED_ROM + NONPAGED_LENGTH))))
				{
					TmpStr.Format("HITTYPE_TBL_ADDR, but HitPagePtr is NULL, and Addr is in paged ROM");
					DebugShiftKeyMsgStrPrint(TmpStr);
					return -1;
				}

				HitBuf[2] = (char)NONPAGED_BANK_INDICATOR;
			}
			else
			{
				HitBuf[2] = (*HitPagePtr)&0xFF;
			}

#if 0
//debug force particular table addr
HitBuf[0] = 0x40;
HitBuf[1] = 0x39;
HitBuf[2] = 0x30;
#endif
			//
			TmpStr.Format("Potential Match. HitType 0x%02x, HitBytes 0x%02x 0x%02x 0x%02x",(*(Ptr-1))&0xFF,(*HitBuf)&0xFF,(*(HitBuf+1))&0xFF,(*(HitBuf+2))&0xFF);
			DebugShiftKeyMsgStrPrint(TmpStr);
			//
			if (GetROMAddressFromAddrOf3ByteWPCAddrPage(HitBuf, pTbl) == 0)
			{
				TmpStr.Format("Table Found!");
				DebugShiftKeyMsgStrPrint(TmpStr);
				return 0;
			}
			//
			TmpStr.Format("Error deriving table addr from hit, HitType 0x%02x, HitBytes 0x%02x 0x%02x 0x%02x. Will keep looking. May need to debug by opening window while pressing <shift>",(*(Ptr-1))&0xFF,(*HitBuf)&0xFF,(*(HitBuf+1))&0xFF,(*(HitBuf+2))&0xFF);
			DebugShiftKeyMsgStrPrint(TmpStr);
			break;

		case HITTYPE_NONE:
			return 0;

		default:
			AfxMessageBox("Unexpected HitType");
			break;
	}
	return -1;
}

int DMD::InitCommon()
{
	CHexEditorDoc *DocPtr = (((CHexEditorView *)((CFrameWnd*)(AfxGetApp()->m_pMainWnd))->GetActiveView())->GetDocument());
	ASSERT_VALID(DocPtr);
	unsigned long Length = DocPtr->m_nBufferLength;


	if ((Length != 0x40000) && (Length != 0x80000) && (Length != 0x100000))
	{
		AfxMessageBox("ROM doesn't appear to be a WPC rom image");
		return -1;
	}

	CommonData.ROMSize = Length;
	CommonData.TotalPages = (unsigned char)((Length + (PAGE_LENGTH - 1)) / PAGE_LENGTH);
	CommonData.StartPtr = DocPtr->m_szDataBuffer.GetBuffer(Length);
    CommonData.EndPtr = (unsigned char *)&CommonData.StartPtr[(CommonData.ROMSize-1)];

	if (CommonData.StartPtr == NULL)
	{
		AfxMessageBox("Unexpected NULL pointer for ROM data");
		return -1;
	}

	CommonData.BasePageIndex = (*CommonData.StartPtr) & 0xFF;

	return 0;
}

#if 0
int DMD::InitGraphics()
{
	// Example assembly for loading graphics table (IJ_L7):
	//-------------------------------------------------------------------------------------------------------------------------
	// EB1A: 34 76       PSHS  U,Y,X,B,A        ; Save U,Y,X,D onto stack
	// EB1C: BE 82 AC    LDX   $82AC            ; Load from Graphic table 82AC into X, 82AC has 4001, Top of Paged RAM
	// EB1F: 30 8B       LEAX  D,X              ; Advance X by D
	// EB21: 58          ASLB                   ; Multiply D by 2
	// EB22: 49          ROLA                   ; Multiply D by 2
	// EB23: 30 8B       LEAX  D,X              ; Advance X by (D * 2)
	// EB25: F6 82 AE    LDB   $82AE            ; Load B with BANK/Page for graphic table from 82AE (0x29)
	// EB28: BD 90 4D    JSR   $904D            ; Get the 2 graphic table entry bytes into Y and advance X pointer by 2.
	// EB2B: BD 90 2B    JSR   $902B            ; Get the 3rd graphic table entry byte into A
	// EB2E: 1F 21       TFR   Y,X              ; Transfer Y to X (2 graphic table entry bytes and the address of the 3rd byte)
	// EB30: 1F 89       TFR   A,B              ; Transfer A to B (3rd graphic table entry byte and the graphic table bank)
	//-------------------------------------------------------------------------------------------------------------------------
	// Search for: BE xx xx 30 8B 58 49 yy yy F6 yy yy F6 yy yy, WPC Table address address is xxxx in non-banked ROM
	// Search for: BE xx xx 30 8B 58 49 yy yy BD yy yy BD yy yy, WPC Table address address is xxxx in non-banked ROM
	// Search for: BE xx xx 30 8B 58 49 yy yy F6 yy yy BD yy yy, WPC Table address address is xxxx in non-banked ROM
	// Search for: BE xx xx 30 8B 58 49 yy yy BD yy yy F6 yy yy, WPC Table address address is xxxx in non-banked ROM
	//
	//
	//
	// Example assembly for loading graphics table (CFTBL_L4):
	//-------------------------------------------------------------------------------------------------------------------------
	// F19C: 34 76       PSHS  U,Y,X,B,A        ; Save registers
	// F19E: EE 68       LDU   $0008,S          ; Get stack
	// F1A0: E6 C4       LDB   ,U               ; Get 1-byte parameter to this function call
	// F1A2: 33 41       LEAU  $0001,U          ; Fixup stack
	// F1A4: EF 68       STU   $0008,S          ; 
	// F1A6: BE 82 8E    LDX   $828E            ; X gets address of graphic table
	// F1A9: 3A          ABX                    ;
	// F1AA: 3A          ABX                    ;
	// F1AB: 3A          ABX                    ;
	// F1AC: D6 11       LDB   $11              ; Get current bank
	// F1AE: 34 04       PSHS  B                ; Save it
	// F1B0: C6 29       LDB   #$29             ; Load fixed number of graphic table bank
	// F1B2: BD 8F D1    JSR   $8FD1            ; Set bank
	//-------------------------------------------------------------------------------------------------------------------------
	// Search for: EE yy E6 C4 33 41 EF yy BE xx xx 3A 3A 3A D6 yy 34 04 C6 zz, WPC Table address address is xxxx in non-banked ROM
	//
	//
	//
	// Example assembly for loading graphics table (FishTales_L5):
	//-------------------------------------------------------------------------------------------------------------------------
	// ECD1: 34 76       PSHS  U,Y,X,B,A        ; Save registers
	// ECD3: EE 68       LDU   $0008,S          ;
	// ECD5: E6 C0       LDB   ,U+              ; Get 1-byte parameter from function call
	// ECD7: EF 68       STU   $0008,S          ;
	// ECD9: BE 82 88    LDX   $8288            ; X gets table address
	// ECDC: 3A          ABX                    ;
	// ECDD: 3A          ABX                    ;
	// ECDE: 3A          ABX                    ;
	// ECDF: D6 11       LDB   $11              ; Get current bank
	// ECE1: 34 04       PSHS  B                ; Save it
	// ECE3: C6 2B       LDB   #$2B             ; Set Table bank value
	// ECE5: BD 91 0D    JSR   $910D            ; Set bank
	//-------------------------------------------------------------------------------------------------------------------------
	// Search for: EE yy E6 C0 EF yy BE xx xx 3A 3A 3A D6 yy 34 04 C6 zz, WPC Table address address is xxxx in non-banked ROM
	//
	//
	//
	//
	// Example assembly for loading graphics table (CFTBL_L4):
	//-------------------------------------------------------------------------------------------------------------------------
	// E8C5: 34 16       PSHS  X,B,A            ; Save registers
	// E8C7: 8E 53 6A    LDX   #$536A           ; X gets address of graphic table
	// E8CA: CB 02       ADDB  #$02             ; 
	// E8CC: 3A          ABX                    ;
	// E8CD: 3A          ABX                    ;
	// E8CE: 3A          ABX                    ;
	// E8CF: D6 13       LDB   $13              ; Get current bank
	// E8D1: 34 04       PSHS  B                ; Save it
	// E8D3: C6 22       LDB   #$22             ; Load fixed number of graphic table bank
	// E8D5: BD 8F E1    JSR   $8FE1            ; Set bank
	//-------------------------------------------------------------------------------------------------------------------------
	// Search for: 34 16 8E xx xx CB yy 3A 3A 3A D6 yy 34 04 C6 zz BD yy yy, WPC Table address is $xxxx,zz
	//
	//
	//
	// Example assembly for loading graphics table (DRWHO_L2):
	//-------------------------------------------------------------------------------------------------------------------------
	// F08F: 34 76       PSHS  U,Y,X,B,A        ; Save registers
	// F091: EE 68       LDU   $0008,S          ;
	// F093: E6 C0       LDB   ,U+              ; Get 1-byte param from function call
	// F095: EF 68       STU   $0008,S          ;
	// F097: 8E 54 BB    LDX   #$54BB           ; X gets table addr
	// F09A: C1 DE       CMPB  #$DE             ;
	// F09C: 25 02       BCS   $F0A0            ;
	// F09E: 3F          SWI                    ;
	// F09F: 5F          CLRB                   ;
	// F0A0: 3A          ABX                    ;
	// F0A1: 3A          ABX                    ;
	// F0A2: 3A          ABX                    ;
	// F0A3: D6 13       LDB   $13              ; Get current bank
	// F0A5: 34 04       PSHS  B                ; Save it
	// F0A7: C6 22       LDB   #$22             ; Set Table bank value
	// F0A9: BD 91 1D    JSR   $911D            ; Set bank
	//-------------------------------------------------------------------------------------------------------------------------
	// Search for: 34 76 EE 68 E6 C0 EF 68 8E xx xx C1 yy 25 02 3F 5F 3A 3A 3A D6 yy 34 04 C6 zz BD, WPC Table address is $xxxx,zz
	//
	//
	//
	// Example assembly for loading graphics table (Gilligan's Island L9):
	//-------------------------------------------------------------------------------------------------------------------------
	// E3E9: 34 76       PSHS  U,Y,X,B,A        ; Save registers
	// E3EB: EE 68       LDU   $0008,S          ;
	// E3ED: E6 C4       LDB   ,U               ; Get 1-byte param from function call
	// E3EF: 33 41       LEAU  $0001,U          ;
	// E3F1: EF 68       STU   $0008,S          ;
	// E3F3: 8E E7 48    LDX   #$E748           ; X gets table addr
	// E3F6: 3A          ABX                    ;
	// E3F7: 3A          ABX                    ;
	// E3F8: 3A          ABX                    ;
	// E3F9: D6 11       LDB   $11              ; Get current bank
	// E3FB: 34 04       PSHS  B                ; Save it
	// E3FD: BD 91 16    JSR   $9116            ; 
	//-------------------------------------------------------------------------------------------------------------------------
	// Search for: 34 76 EE 68 E6 C4 33 41 EF 68 8E xx xx 3A 3A 3A D6 yy 34 04 BD, WPC Table address is xxxx in non-banked ROM
	//
	//
	//
	// Example assembly for loading graphics table (Gilligan's Island L9):
	//-------------------------------------------------------------------------------------------------------------------------
	// E7EB: 34 76       PSHS  U,Y,X,B,A        ;
	// E7ED: EE 68       LDU   $0008,S          ; 
	// E7EF: E6 C4       LDB   ,U               ;
	// E7F1: 33 41       LEAU  $0001,U          ;
	// E7F3: EF 68       STU   $0008,S          ;
	// E7F5: BE 82 2D    LDX   $822D            ;
	// E7F8: 3A          ABX                    ;
	// E7F9: 3A          ABX                    ;
	// E7FA: 3A          ABX                    ;
	// E7FB: D6 12       LDB   $12              ;
	// E7FD: 34 04       PSHS  B                ;
	// E7FF: BD 90 C0    JSR   $90C0            ;
	//-------------------------------------------------------------------------------------------------------------------------
	// Search for: 34 76 EE 68 E6 C4 33 41 EF 68 BE xx xx 3A 3A 3A D6 yy 34 04 BD, WPC Table address address is xxxx in non-banked ROM
	//
	//
	// Example assembly for loading graphics table (Hurricane_L2):
	//-------------------------------------------------------------------------------------------------------------------------
	// FB79: 34 76       PSHS  U,Y,X,B,A        ; Save registers
	// FB7B: EE 68       LDU   $0008,S          ;
	// FB7D: E6 C0       LDB   ,U+              ;
	// FB7F: EF 68       STU   $0008,S          ;
	// FB81: BE 82 63    LDX   $8263            ;
	// FB84: 30 89 03 00 LEAX  $0300,X          ;
	// FB88: 3A          ABX                    ;
	// FB89: 3A          ABX                    ;
	// FB8A: 3A          ABX                    ;
	// FB8B: D6 14       LDB   $14              ;
	// FB8D: 34 04       PSHS  B                ;
	// FB8F: BD 91 41    JSR   $9141            ;
	//-------------------------------------------------------------------------------------------------------------------------
	// Search for: 34 76 EE 68 E6 C0 EF 68 BE xx xx 30 89 yy yy 3A 3A 3A D6 yy 34 04 BD, WPC Table address address address is xxxx in non-banked ROM
	//
	//
	//
	// Example assembly for loading graphics table (AddamsFamily_H4):
	//-------------------------------------------------------------------------------------------------------------------------
	// E456: 34 76       PSHS  U,Y,X,B,A        ; Save registers
	// E458: EE 68       LDU   $0008,S          ;
	// E45A: E6 C0       LDB   ,U+              ;
	// E45C: EF 68       STU   $0008,S          ;
	// E45E: 8E E5 91    LDX   #$E591           ;
	// E461: 20 0F       BRA   $E472            ;
	// E463: CF 74                              ;
	// E465: 34 76       PSHS  U,Y,X,B,A        ; Save registers
	// E467: EE 68       LDU   $0008,S          ;
	// E469: E6 C4       LDB   ,U               ;
	// E46B: 33 41       LEAU  $0001,U          ;
	// E46D: EF 68       STU   $0008,S          ;
	// E46F: 8E E7 56    LDX   #$E756           ;
	// E472: 3A          ABX                    ;
	// E473: 3A          ABX                    ;
	// E474: 3A          ABX                    ;
	// E475: D6 11       LDB   $11              ;
	// E477: 34 04       PSHS  B                ;
	// E479: BD 90 46    JSR   $9046            ;
	//-------------------------------------------------------------------------------------------------------------------------
	// Search for: 34 76 EE 68 E6 C0 EF 68 8E xx xx 20 0F yy yy 34 76 EE 68 E6 C4 33 41 EF 68 8E yy yy 3A 3A 3A D6 zz 34 04 BD, WPC Table address is xxxx in non-banked ROM
	//
	//
	//
	// Example assembly for loading graphics table (AddamsFamilyGold_H3):
	//-------------------------------------------------------------------------------------------------------------------------
	// E322: 34 76       PSHS  U,Y,X,B,A        ;
	// E324: EE 68       LDU   $0008,S          ;
	// E326: E6 C0       LDB   ,U+              ;
	// E328: EF 68       STU   $0008,S          ;
	// E32A: 8E 40 01    LDX   #$4001           ;
	// E32D: 20 0F       BRA   $E33E            ;
	// E32F: CF 74                              ;
	// E331: 34 76       PSHS  U,Y,X,B,A        ;
	// E333: EE 68       LDU   $0008,S          ;
	// E335: E6 C4       LDB   ,U               ;
	// E337: 33 41       LEAU  $0001,U          ;
	// E339: EF 68       STU   $0008,S          ;
	// E33B: 8E 42 80    LDX   #$4280           ;
	// E33E: 3A          ABX                    ;
	// E33F: 3A          ABX                    ;
	// E340: 3A          ABX                    ;
	// E341: D6 11       LDB   $11              ;
	// E343: 34 04       PSHS  B                ;
	// E345: C6 36       LDB   #$36             ;
	// E347: BD 90 3A    JSR   $903A            ;
	//-------------------------------------------------------------------------------------------------------------------------
	// Search for: 34 76 EE 68 E6 C0 EF 68 8E xx xx 20 0F yy yy 34 76 EE 68 E6 C4 33 41 EF 68 8E yy yy 3A 3A 3A D6 zz 34 04 C6 zz BD, WPC Table address is $xxxx,zz in banked ROM
	//
	//
	//
	// Example assembly for loading graphics table (BlackRose_L4):
	//-------------------------------------------------------------------------------------------------------------------------
	// EE51: 34 76       PSHS  U,Y,X,B,A        ;
	// EE53: EE 68       LDU   $0008,S          ;
	// EE55: E6 C4       LDB   ,U               ;
	// EE57: 33 41       LEAU  $0001,U          ;
	// EE59: EF 68       STU   $0008,S          ;
	// EE5B: 8E E8 B2    LDX   #$E8B2           ;
	// EE5E: 20 0D       BRA   $EE6D            ;
	// EE60: 34 76       PSHS  U,Y,X,B,A        ;
	// EE62: EE 68       LDU   $0008,S          ;
	// EE64: E6 C4       LDB   ,U               ;
	// EE66: 33 41       LEAU  $0001,U          ;
	// EE68: EF 68       STU   $0008,S          ;
	// EE6A: BE 82 88    LDX   $8288            ;
	// EE6D: 3A          ABX                    ;
	// EE6E: 3A          ABX                    ;
	// EE6F: 3A          ABX                    ;
	// EE70: D6 11       LDB   $11              ;
	// EE72: 34 04       PSHS  B                ;
	// EE74: BD 91 16    JSR   $9116            ;
	//-------------------------------------------------------------------------------------------------------------------------
	// Search for: 34 76 EE 68 E6 C4 33 41 EF 68 8E yy yy 20 yy 34 76 EE 68 E6 C4 33 41 EF 68 BE xx xx 3A 3A 3A D6 zz 34 04 BD, WPC Table address address address is xxxx in non-banked ROM
	//
	//
	//
	// Example assembly for loading graphics table (Terminator2_L8):
	//-------------------------------------------------------------------------------------------------------------------------
	// EF40: 34 76       PSHS  U,Y,X,B,A        ;
	// EF42: 8E 40 01    LDX   #$4001           ;
	// EF45: 20 0B       BRA   $EF52            ;
	// EF47: 34 76       PSHS  U,Y,X,B,A        ;
	// EF49: EE 68       LDU   $0008,S          ;
	// EF4B: E6 C0       LDB   ,U+              ;
	// EF4D: EF 68       STU   $0008,S          ;
	// EF4F: 8E 40 01    LDX   #$4001           ;
	// EF52: 3A          ABX                    ;
	// EF53: 3A          ABX                    ;
	// EF54: 3A          ABX                    ;
	// EF55: D6 11       LDB   $11              ;
	// EF57: 34 04       PSHS  B                ;
	// EF59: C6 22       LDB   #$22             ;
	// EF5B: BD 90 BC    JSR   $90BC            ;
	//-------------------------------------------------------------------------------------------------------------------------
	// Search for: 34 76 8E xx xx 20 0B 34 76 EE 68 E6 C0 EF 68 8E yy yy 3A 3A 3A D6 yy 34 04 C6 zz BD, WPC Table address is $xxxx,zz
	//
	//
	//
	// Example assembly for loading graphics table (Getaway_L5):
	//-------------------------------------------------------------------------------------------------------------------------
	// F540: 34 76       PSHS  U,Y,X,B,A        ;
	// F542: 8E 42 41    LDX   #$4241           ;
	// F545: 20 07       BRA   $F54E            ;
	// F547: 34 76       PSHS  U,Y,X,B,A        ;
	// F549: 8E 40 01    LDX   #$4001           ;
	// F54C: 20 00       BRA   $F54E            ;
	// F54E: 3A          ABX                    ;
	// F54F: 3A          ABX                    ;
	// F550: 3A          ABX                    ;
	// F551: D6 11       LDB   $11              ;
	// F553: 34 04       PSHS  B                ;
	// F555: C6 2F       LDB   #$2F             ;
	// F557: BD 91 0D    JSR   $910D            ;
	//-------------------------------------------------------------------------------------------------------------------------
	// Search for: 34 76 8E xx xx 20 00 3A 3A 3A D6 11 34 04 C6 yy BD, WPC Table address $xxxx,yy
	//
	//
	//
	// Example assembly for loading graphics table (Whitewater_L5):  *** Special, unique coding ***
	//-------------------------------------------------------------------------------------------------------------------------
	// 6653: BD D4 4D    JSR   $D44D            ;
	// 6656: CE 44 4A    LDU   #$444A           ; Address of Graphics Table itself, $E5B7 knows to set bank to 0x26
	// 6659: BD E5 B7    JSR   $E5B7		 ;
	// 665C: 00 1F       NEG   $1F
	//-------------------------------------------------------------------------------------------------------------------------
	// E5B7: 34 76       PSHS  U,Y,X,B,A        ;
	// E5B9: 1F 31       TFR   U,X              ;
	// E5BB: EE 68       LDU   $0008,S          ;
	// E5BD: E6 C0       LDB   ,U+              ;
	// E5BF: EF 68       STU   $0008,S          ;
	// E5C1: 20 0C       BRA   $E5CF            ;
	// E5C3: 34 76       PSHS  U,Y,X,B,A        ; 
	// E5C5: 1F 31       TFR   U,X              ;
	// E5C7: 20 06       BRA   $E5CF            ;
	// E5C9: 34 76       PSHS  U,Y,X,B,A        ;
	// E5CB: 1F 89       TFR   A,B              ;
	// E5CD: 1F 31       TFR   U,X              ;
	// E5CF: 3A          ABX                    ;
	// E5D0: 3A          ABX                    ;
	// E5D1: 3A          ABX                    ;
	// E5D2: D6 11       LDB   $11              ;
	// E5D4: 34 04       PSHS  B                ;
	// E5D6: C6 26       LDB   #$26             ;
	// E5D8: BD 8F E9    JSR   $8FE9            ;
	//-------------------------------------------------------------------------------------------------------------------------
	// Search for: 34 76 1F 31 EE 68 E6 C0 EF 68 20 0C 34 76 1F 31 20 06 34 76 1F 89 1F 31 3A 3A 3A D6 zz 34 04 C6 26 BD yy yy
	// Then Search entire ROM for: BD yy yy CE xx xx BD ww ww 00, where $wwww is address if previous line. WPC Table Address is $xxxx,zz
    //
	//
	int Page,PageByteIdx;
	LPTSTR Ptr = CommonData.StartPtr;
	LPTSTR HitTablePtr,HitPagePtr;
	int HitType,HitId;

	TmpStr.Format("Searching ROM for Master Graphic Table Address");
	DebugShiftKeyMsgStrPrint(TmpStr);

	for (Page = 0; Page < CommonData.TotalPages; Page++)
	{
		for (PageByteIdx = 0; PageByteIdx < PAGE_LENGTH; PageByteIdx++)
		{
			HitType = HITTYPE_NONE;
			HitTablePtr = HitPagePtr = NULL;
			HitId = 1;

			switch ((*Ptr++) & 0xFF)
			{
				case 0xBE :
					//
					//             -1 +0 +1  2  3  4  5  6  7  8  9 10 11 12 13
					// Search for: BE xx xx 30 8B 58 49 yy yy F6 yy yy F6 yy yy, WPC Table address address is xxxx in non-banked ROM
					// Search for: BE xx xx 30 8B 58 49 yy yy BD yy yy BD yy yy, WPC Table address address is xxxx in non-banked ROM
					// Search for: BE xx xx 30 8B 58 49 yy yy F6 yy yy BD yy yy, WPC Table address address is xxxx in non-banked ROM
					// Search for: BE xx xx 30 8B 58 49 yy yy BD yy yy F6 yy yy, WPC Table address address is xxxx in non-banked ROM
					//
					if (PageByteIdx >= (PAGE_LENGTH-16)) // don't try to read out of bounds, going to read up to 16 bytes after Ptr
					{
						break;
					}
					if (((*(Ptr+2) & 0xFF) == 0x30) &&
						((*(Ptr+3) & 0xFF) == 0x8B) &&
						((*(Ptr+4) & 0xFF) == 0x58) &&
						((*(Ptr+5) & 0xFF) == 0x49) &&
						(((*(Ptr+8) & 0xFF) == 0xF6) || ((*(Ptr+9) & 0xFF) == 0xBD)) &&
						(((*(Ptr+11) & 0xFF) == 0xBD) || ((*(Ptr+12) & 0xFF) == 0xF6)))
					{
						//
						HitType = HITTYPE_TBL_ADDR_ADDR;
						HitTablePtr = Ptr;
						//
						//TmpStr.Format("0x%02X HitId %d",(*(Ptr-1))&0xFF,HitId);
						//DebugShiftKeyMsgStrPrint(TmpStr);
					}
					//HitId++;
					break;

				case 0xEE:
					//
					//             -1 +0 +1  2  3  4  5  6  7  8  9 10 11 12 13 14 15 16 17 18
					// Search for: EE yy E6 C4 33 41 EF yy BE xx xx 3A 3A 3A D6 yy 34 04 C6 zz, WPC Table address address is xxxx in non-banked ROM
					if (PageByteIdx >= (PAGE_LENGTH-32)) // don't try to read out of bounds, going to read up to 16 bytes after Ptr
					{
						break;
					}
					if (((*(Ptr+1) & 0xFF) == 0xE6) &&
						((*(Ptr+2) & 0xFF) == 0xC4) &&
						((*(Ptr+3) & 0xFF) == 0x33) &&
						((*(Ptr+4) & 0xFF) == 0x41) &&
						((*(Ptr+5) & 0xFF) == 0xEF) &&
						((*(Ptr+7) & 0xFF) == 0xBE) &&
						((*(Ptr+10) & 0xFF) == 0x3A) &&
						((*(Ptr+11) & 0xFF) == 0x3A) &&
						((*(Ptr+12) & 0xFF) == 0x3A) &&
						((*(Ptr+13) & 0xFF) == 0xD6) &&
						((*(Ptr+15) & 0xFF) == 0x34) &&
						((*(Ptr+16) & 0xFF) == 0x04) &&
						((*(Ptr+17) & 0xFF) == 0xC6))
					{
						//
						HitType = HITTYPE_TBL_ADDR_ADDR;
						HitTablePtr = Ptr+8;
						//
						TmpStr.Format("0xEE HitId %d",HitId);
						DebugShiftKeyMsgStrPrint(TmpStr);
					}
					HitId++;
					//
					//---------------------------------------------------------------------------------------------------------
					//---------------------------------------------------------------------------------------------------------
					//
					//             -1 +0 +1  2  3  4  5  6  7  8  9 10 11 12 13 14 15 16
					// Search for: EE yy E6 C0 EF yy BE xx xx 3A 3A 3A D6 yy 34 04 C6 zz, WPC Table address address is xxxx in non-banked ROM
					if (((*(Ptr+1) & 0xFF) == 0xE6) &&
						((*(Ptr+2) & 0xFF) == 0xC0) &&
						((*(Ptr+3) & 0xFF) == 0xEF) &&
						((*(Ptr+5) & 0xFF) == 0xBE) &&
						((*(Ptr+8) & 0xFF) == 0x3A) &&
						((*(Ptr+9) & 0xFF) == 0x3A) &&
						((*(Ptr+10) & 0xFF) == 0x3A) &&
						((*(Ptr+11) & 0xFF) == 0xD6) &&
						((*(Ptr+13) & 0xFF) == 0x34) &&
						((*(Ptr+14) & 0xFF) == 0x04) &&
						((*(Ptr+15) & 0xFF) == 0xC6))
					{
						//
						HitType = HITTYPE_TBL_ADDR_ADDR;
						HitTablePtr = Ptr+6;
						//
						TmpStr.Format("0x%02X HitId %d",(*(Ptr-1))&0xFF,HitId);
						DebugShiftKeyMsgStrPrint(TmpStr);
					}
					//HitId++;
					break;

				case 0x34:
					//
					//             -1 +0 +1  2  3  4  5  6  7  8  9 10 11 12 13 14 15 16 17
					// Search for: 34 16 8E xx xx CB yy 3A 3A 3A D6 yy 34 04 C6 zz BD yy yy, WPC Table address is $xxxx,zz
					// Search for: 34 16 8E xx xx CB yy 3A 3A 3A D6 yy 34 04 C6 zz F6 yy yy, WPC Table address is $xxxx,zz

					if (PageByteIdx >= (PAGE_LENGTH-32)) // don't try to read out of bounds, going to read up to 16 bytes after Ptr
					{
						break;
					}
					if (((*(Ptr+0) & 0xFF) == 0x16) &&
						((*(Ptr+1) & 0xFF) == 0x8E) &&
						((*(Ptr+4) & 0xFF) == 0xCB) &&
						((*(Ptr+6) & 0xFF) == 0x3A) &&
						((*(Ptr+7) & 0xFF) == 0x3A) &&
						((*(Ptr+8) & 0xFF) == 0x3A) &&
						((*(Ptr+9) & 0xFF) == 0xD6) &&
						((*(Ptr+11) & 0xFF) == 0x34) &&
						((*(Ptr+12) & 0xFF) == 0x04) &&
						((*(Ptr+13) & 0xFF) == 0xC6) &&
						(((*(Ptr+15) & 0xFF) == 0xBD) || ((*(Ptr+15) & 0xFF) == 0xF6)))
					{
						//
						HitType = HITTYPE_TBL_ADDR;
						HitTablePtr = Ptr+2;
						HitPagePtr = Ptr+14;
						//
						TmpStr.Format("0x%02X HitId %d",(*(Ptr-1))&0xFF,HitId);
						DebugShiftKeyMsgStrPrint(TmpStr);
					}
					HitId++;
					//
					//---------------------------------------------------------------------------------------------------------
					//---------------------------------------------------------------------------------------------------------
					//
					//             -1 +0 +1  2  3  4  5  6  7  8  9 10 11 12 13 14 15 16 17 18 19 20 21 22 23 24 25
					// Search for: 34 76 EE 68 E6 C0 EF 68 8E xx xx C1 yy 25 02 3F 5F 3A 3A 3A D6 yy 34 04 C6 zz BD, WPC Table address is $xxxx,zz
					if (((*(Ptr+0) & 0xFF) == 0x76) &&
						((*(Ptr+1) & 0xFF) == 0xEE) &&
						((*(Ptr+2) & 0xFF) == 0x68) &&
						((*(Ptr+3) & 0xFF) == 0xE6) &&
						((*(Ptr+4) & 0xFF) == 0xC0) &&
						((*(Ptr+5) & 0xFF) == 0xEF) &&
						((*(Ptr+6) & 0xFF) == 0x68) &&
						((*(Ptr+7) & 0xFF) == 0x8E) &&
						((*(Ptr+10) & 0xFF) == 0xC1) &&
						((*(Ptr+12) & 0xFF) == 0x25) &&
						((*(Ptr+13) & 0xFF) == 0x02) &&
						((*(Ptr+14) & 0xFF) == 0x3F) &&
						((*(Ptr+15) & 0xFF) == 0x5F) &&
						((*(Ptr+16) & 0xFF) == 0x3A) &&
						((*(Ptr+17) & 0xFF) == 0x3A) &&
						((*(Ptr+18) & 0xFF) == 0x3A) &&
						((*(Ptr+19) & 0xFF) == 0xD6) &&
						((*(Ptr+21) & 0xFF) == 0x34) &&
						((*(Ptr+22) & 0xFF) == 0x04) &&
						((*(Ptr+23) & 0xFF) == 0xC6) &&
						(((*(Ptr+25) & 0xFF) == 0xBD) || ((*(Ptr+25) & 0xFF) == 0xF6)))
					{
						//
						HitType = HITTYPE_TBL_ADDR;
						HitTablePtr = Ptr+8;
						HitPagePtr = Ptr+24;
						//
						TmpStr.Format("0x%02X HitId %d",(*(Ptr-1))&0xFF,HitId);
						DebugShiftKeyMsgStrPrint(TmpStr);
					}
					HitId++;
					//
					//---------------------------------------------------------------------------------------------------------
					//---------------------------------------------------------------------------------------------------------
					//
					//             -1 +0 +1  2  3  4  5  6  7  8  9 10 11 12 13 14 15 16 17 18 19
					// Search for: 34 76 EE 68 E6 C4 33 41 EF 68 8E xx xx 3A 3A 3A D6 yy 34 04 BD, WPC Table address is xxxx in non-banked ROM
					if (((*(Ptr+0) & 0xFF) == 0x76) &&
						((*(Ptr+1) & 0xFF) == 0xEE) &&
						((*(Ptr+2) & 0xFF) == 0x68) &&
						((*(Ptr+3) & 0xFF) == 0xE6) &&
						((*(Ptr+4) & 0xFF) == 0xC4) &&
						((*(Ptr+5) & 0xFF) == 0x33) &&
						((*(Ptr+6) & 0xFF) == 0x41) &&
						((*(Ptr+7) & 0xFF) == 0xEF) &&
						((*(Ptr+8) & 0xFF) == 0x68) &&
						((*(Ptr+9) & 0xFF) == 0x8E) &&
						((*(Ptr+12) & 0xFF) == 0x3A) &&
						((*(Ptr+13) & 0xFF) == 0x3A) &&
						((*(Ptr+14) & 0xFF) == 0x3A) &&
						((*(Ptr+15) & 0xFF) == 0xD6) &&
						((*(Ptr+17) & 0xFF) == 0x34) &&
						((*(Ptr+18) & 0xFF) == 0x04) &&
						((*(Ptr+19) & 0xFF) == 0xBD))
					{
						//
						HitType = HITTYPE_TBL_ADDR;
						HitTablePtr = Ptr+10;
						//
						TmpStr.Format("0x%02X HitId %d",(*(Ptr-1))&0xFF,HitId);
						DebugShiftKeyMsgStrPrint(TmpStr);
					}
					HitId++;
					//
					//---------------------------------------------------------------------------------------------------------
					//---------------------------------------------------------------------------------------------------------
					//
					//             -1 +0 +1  2  3  4  5  6  7  8  9 10 11 12 13 14 15 16 17 18 19
					// Search for: 34 76 EE 68 E6 C4 33 41 EF 68 BE xx xx 3A 3A 3A D6 yy 34 04 BD, WPC Table address address is xxxx in non-banked ROM
					if (((*(Ptr+0) & 0xFF) == 0x76) &&
						((*(Ptr+1) & 0xFF) == 0xEE) &&
						((*(Ptr+2) & 0xFF) == 0x68) &&
						((*(Ptr+3) & 0xFF) == 0xE6) &&
						((*(Ptr+4) & 0xFF) == 0xC4) &&
						((*(Ptr+5) & 0xFF) == 0x33) &&
						((*(Ptr+6) & 0xFF) == 0x41) &&
						((*(Ptr+7) & 0xFF) == 0xEF) &&
						((*(Ptr+8) & 0xFF) == 0x68) &&
						((*(Ptr+9) & 0xFF) == 0xBE) &&
						((*(Ptr+12) & 0xFF) == 0x3A) &&
						((*(Ptr+13) & 0xFF) == 0x3A) &&
						((*(Ptr+14) & 0xFF) == 0x3A) &&
						((*(Ptr+15) & 0xFF) == 0xD6) &&
						((*(Ptr+17) & 0xFF) == 0x34) &&
						((*(Ptr+18) & 0xFF) == 0x04) &&
						((*(Ptr+19) & 0xFF) == 0xBD))
					{
						//
						HitType = HITTYPE_TBL_ADDR_ADDR;
						HitTablePtr = Ptr+10;
						//
						TmpStr.Format("0x%02X HitId %d",(*(Ptr-1))&0xFF,HitId);
						DebugShiftKeyMsgStrPrint(TmpStr);
					}
					HitId++;
					//
					//---------------------------------------------------------------------------------------------------------
					//---------------------------------------------------------------------------------------------------------
					//
					//             -1 +0 +1  2  3  4  5  6  7  8  9 10 11 12 13 14 15 16 17 18 19 20 21
					// Search for: 34 76 EE 68 E6 C0 EF 68 BE xx xx 30 89 yy yy 3A 3A 3A D6 yy 34 04 BD, WPC Table address address address is xxxx in non-banked ROM
					if (((*(Ptr+0) & 0xFF) == 0x76) &&
						((*(Ptr+1) & 0xFF) == 0xEE) &&
						((*(Ptr+2) & 0xFF) == 0x68) &&
						((*(Ptr+3) & 0xFF) == 0xE6) &&
						((*(Ptr+4) & 0xFF) == 0xC0) &&
						((*(Ptr+5) & 0xFF) == 0xEF) &&
						((*(Ptr+6) & 0xFF) == 0x68) &&
						((*(Ptr+7) & 0xFF) == 0xBE) &&
						((*(Ptr+10) & 0xFF) == 0x30) &&
						((*(Ptr+11) & 0xFF) == 0x89) &&
						((*(Ptr+14) & 0xFF) == 0x3A) &&
						((*(Ptr+15) & 0xFF) == 0x3A) &&
						((*(Ptr+16) & 0xFF) == 0x3A) &&
						((*(Ptr+17) & 0xFF) == 0xD6) &&
						((*(Ptr+19) & 0xFF) == 0x34) &&
						((*(Ptr+20) & 0xFF) == 0x04) &&
						((*(Ptr+21) & 0xFF) == 0xBD))
					{
						//
						HitType = HITTYPE_TBL_ADDR_ADDR;
						HitTablePtr = Ptr+8;
						//
						TmpStr.Format("0x%02X HitId %d",(*(Ptr-1))&0xFF,HitId);
						DebugShiftKeyMsgStrPrint(TmpStr);
					}
					HitId++;
					//
					//---------------------------------------------------------------------------------------------------------
					//---------------------------------------------------------------------------------------------------------
					//
					//             -1 +0  +1 2  3  4  5  6  7  8  9 10 11 12 13 14 15 16 17 18 19 20 21 22 23 24 25 26 27 28 29 30 31 32 33 34
					// Search for: 34 76 EE 68 E6 C0 EF 68 8E xx xx 20 0F yy yy 34 76 EE 68 E6 C4 33 41 EF 68 8E yy yy 3A 3A 3A D6 zz 34 04 BD, WPC Table address is xxxx in non-banked ROM
					if (((*(Ptr+0) & 0xFF) == 0x76) &&
						((*(Ptr+1) & 0xFF) == 0xEE) &&
						((*(Ptr+2) & 0xFF) == 0x68) &&
						((*(Ptr+3) & 0xFF) == 0xE6) &&
						((*(Ptr+4) & 0xFF) == 0xC0) &&
						((*(Ptr+5) & 0xFF) == 0xEF) &&
						((*(Ptr+6) & 0xFF) == 0x68) &&
						((*(Ptr+7) & 0xFF) == 0x8E) &&
						((*(Ptr+10) & 0xFF) == 0x20) &&
						((*(Ptr+11) & 0xFF) == 0x0F) &&
						((*(Ptr+14) & 0xFF) == 0x34) &&
						((*(Ptr+15) & 0xFF) == 0x76) &&
						((*(Ptr+16) & 0xFF) == 0xEE) &&
						((*(Ptr+17) & 0xFF) == 0x68) &&
						((*(Ptr+18) & 0xFF) == 0xE6) &&
						((*(Ptr+19) & 0xFF) == 0xC4) &&
						((*(Ptr+20) & 0xFF) == 0x33) &&
						((*(Ptr+21) & 0xFF) == 0x41) &&
						((*(Ptr+22) & 0xFF) == 0xEF) &&
						((*(Ptr+23) & 0xFF) == 0x68) &&
						((*(Ptr+24) & 0xFF) == 0x8E) &&
						((*(Ptr+27) & 0xFF) == 0x3A) &&
						((*(Ptr+28) & 0xFF) == 0x3A) &&
						((*(Ptr+29) & 0xFF) == 0x3A) &&
						((*(Ptr+30) & 0xFF) == 0xD6) &&
						((*(Ptr+32) & 0xFF) == 0x34) &&
						((*(Ptr+33) & 0xFF) == 0x04) &&
						((*(Ptr+34) & 0xFF) == 0xBD))
					{
						//
						HitType = HITTYPE_TBL_ADDR;
						HitTablePtr = Ptr+8;
						//
						TmpStr.Format("0x%02X HitId %d",(*(Ptr-1))&0xFF,HitId);
						DebugShiftKeyMsgStrPrint(TmpStr);
					}
					HitId++;
					//
					//---------------------------------------------------------------------------------------------------------
					//---------------------------------------------------------------------------------------------------------
					//
					//             -1 +0  +1 2  3  4  5  6  7  8  9 10 11 12 13 14 15 16 17 18 19 20 21 22 23 24 25 26 27 28 29 30 31 32 33 34 35 36
					// Search for: 34 76 EE 68 E6 C0 EF 68 8E xx xx 20 0F yy yy 34 76 EE 68 E6 C4 33 41 EF 68 8E yy yy 3A 3A 3A D6 zz 34 04 C6 zz BD, WPC Table address is $xxxx,zz in banked ROM
					if (((*(Ptr+0) & 0xFF) == 0x76) &&
						((*(Ptr+1) & 0xFF) == 0xEE) &&
						((*(Ptr+2) & 0xFF) == 0x68) &&
						((*(Ptr+3) & 0xFF) == 0xE6) &&
						((*(Ptr+4) & 0xFF) == 0xC0) &&
						((*(Ptr+5) & 0xFF) == 0xEF) &&
						((*(Ptr+6) & 0xFF) == 0x68) &&
						((*(Ptr+7) & 0xFF) == 0x8E) &&
						((*(Ptr+10) & 0xFF) == 0x20) &&
						((*(Ptr+11) & 0xFF) == 0x0F) &&
						((*(Ptr+14) & 0xFF) == 0x34) &&
						((*(Ptr+15) & 0xFF) == 0x76) &&
						((*(Ptr+16) & 0xFF) == 0xEE) &&
						((*(Ptr+17) & 0xFF) == 0x68) &&
						((*(Ptr+18) & 0xFF) == 0xE6) &&
						((*(Ptr+19) & 0xFF) == 0xC4) &&
						((*(Ptr+20) & 0xFF) == 0x33) &&
						((*(Ptr+21) & 0xFF) == 0x41) &&
						((*(Ptr+22) & 0xFF) == 0xEF) &&
						((*(Ptr+23) & 0xFF) == 0x68) &&
						((*(Ptr+24) & 0xFF) == 0x8E) &&
						((*(Ptr+27) & 0xFF) == 0x3A) &&
						((*(Ptr+28) & 0xFF) == 0x3A) &&
						((*(Ptr+29) & 0xFF) == 0x3A) &&
						((*(Ptr+30) & 0xFF) == 0xD6) &&
						((*(Ptr+32) & 0xFF) == 0x34) &&
						((*(Ptr+33) & 0xFF) == 0x04) &&
						((*(Ptr+34) & 0xFF) == 0xC6) &&
						((*(Ptr+36) & 0xFF) == 0xBD))
					{
						//
						HitType = HITTYPE_TBL_ADDR;
						HitTablePtr = Ptr+8;
						HitPagePtr = Ptr+35;
						//
						TmpStr.Format("0x%02X HitId %d",(*(Ptr-1))&0xFF,HitId);
						DebugShiftKeyMsgStrPrint(TmpStr);
					}
					HitId++;
					//
					//---------------------------------------------------------------------------------------------------------
					//---------------------------------------------------------------------------------------------------------
					//
					//             -1 +0 +1  2  3  4  5  6  7  8  9 10 11 12 13 14 15 16 17 18 19 20 21 22 23 24 25 26 27 28 29 30 31 32 33 34
					// Search for: 34 76 EE 68 E6 C4 33 41 EF 68 8E yy yy 20 yy 34 76 EE 68 E6 C4 33 41 EF 68 BE xx xx 3A 3A 3A D6 zz 34 04 BD, WPC Table address address address is xxxx in non-banked ROM
					if (((*(Ptr+0) & 0xFF) == 0x76) &&
						((*(Ptr+1) & 0xFF) == 0xEE) &&
						((*(Ptr+2) & 0xFF) == 0x68) &&
						((*(Ptr+3) & 0xFF) == 0xE6) &&
						((*(Ptr+4) & 0xFF) == 0xC4) &&
						((*(Ptr+5) & 0xFF) == 0x33) &&
						((*(Ptr+6) & 0xFF) == 0x41) &&
						((*(Ptr+7) & 0xFF) == 0xEF) &&
						((*(Ptr+8) & 0xFF) == 0x68) &&
						((*(Ptr+9) & 0xFF) == 0x8E) &&
						((*(Ptr+12) & 0xFF) == 0x20) &&
						((*(Ptr+14) & 0xFF) == 0x34) &&
						((*(Ptr+15) & 0xFF) == 0x76) &&
						((*(Ptr+16) & 0xFF) == 0xEE) &&
						((*(Ptr+17) & 0xFF) == 0x68) &&
						((*(Ptr+18) & 0xFF) == 0xE6) &&
						((*(Ptr+19) & 0xFF) == 0xC4) &&
						((*(Ptr+20) & 0xFF) == 0x33) &&
						((*(Ptr+21) & 0xFF) == 0x41) &&
						((*(Ptr+22) & 0xFF) == 0xEF) &&
						((*(Ptr+23) & 0xFF) == 0x68) &&
						((*(Ptr+24) & 0xFF) == 0xBE) &&
						((*(Ptr+27) & 0xFF) == 0x3A) &&
						((*(Ptr+28) & 0xFF) == 0x3A) &&
						((*(Ptr+29) & 0xFF) == 0x3A) &&
						((*(Ptr+30) & 0xFF) == 0xD6) &&
						((*(Ptr+32) & 0xFF) == 0x34) &&
						((*(Ptr+33) & 0xFF) == 0x04) &&
						((*(Ptr+34) & 0xFF) == 0xBD))
					{
						//
						HitType = HITTYPE_TBL_ADDR_ADDR;
						HitTablePtr = Ptr+25;
						//
						TmpStr.Format("0x%02X HitId %d",(*(Ptr-1))&0xFF,HitId);
						DebugShiftKeyMsgStrPrint(TmpStr);
					}
					HitId++;
					//
					//---------------------------------------------------------------------------------------------------------
					//---------------------------------------------------------------------------------------------------------
					//
					//             -1 +0 +1  2  3  4  5  6  7  8  9 10 11 12 13 14 15 16 17 18 19 20 21 22 23 24 25 26
					// Search for: 34 76 8E xx xx 20 0B 34 76 EE 68 E6 C0 EF 68 8E yy yy 3A 3A 3A D6 yy 34 04 C6 zz BD, WPC Table address is $xxxx,zz
					if (((*(Ptr+0) & 0xFF) == 0x76) &&
						((*(Ptr+1) & 0xFF) == 0x8E) &&
						((*(Ptr+4) & 0xFF) == 0x20) &&
						((*(Ptr+5) & 0xFF) == 0x0B) &&
						((*(Ptr+6) & 0xFF) == 0x34) &&
						((*(Ptr+7) & 0xFF) == 0x76) &&
						((*(Ptr+8) & 0xFF) == 0xEE) &&
						((*(Ptr+9) & 0xFF) == 0x68) &&
						((*(Ptr+10) & 0xFF) == 0xE6) &&
						((*(Ptr+11) & 0xFF) == 0xC0) &&
						((*(Ptr+12) & 0xFF) == 0xEF) &&
						((*(Ptr+13) & 0xFF) == 0x68) &&
						((*(Ptr+14) & 0xFF) == 0x8E) &&
						((*(Ptr+17) & 0xFF) == 0x3A) &&
						((*(Ptr+18) & 0xFF) == 0x3A) &&
						((*(Ptr+19) & 0xFF) == 0x3A) &&
						((*(Ptr+20) & 0xFF) == 0xD6) &&
						((*(Ptr+22) & 0xFF) == 0x34) &&
						((*(Ptr+23) & 0xFF) == 0x04) &&
						((*(Ptr+24) & 0xFF) == 0xC6) &&
						((*(Ptr+26) & 0xFF) == 0xBD))
					{
						//
						HitType = HITTYPE_TBL_ADDR;
						HitTablePtr = Ptr+2;
						HitPagePtr = Ptr+25;
						//
						TmpStr.Format("0x%02X HitId %d",(*(Ptr-1))&0xFF,HitId);
						DebugShiftKeyMsgStrPrint(TmpStr);
					}
					HitId++;
					//
					//---------------------------------------------------------------------------------------------------------
					//---------------------------------------------------------------------------------------------------------
					//
					//             -1 +0 +1  2  3  4  5  6  7  8  9 10 11 12 13 14 15
					// Search for: 34 76 8E xx xx 20 00 3A 3A 3A D6 11 34 04 C6 yy BD, WPC Table address $xxxx,yy
					if (((*(Ptr+0) & 0xFF) == 0x76) &&
						((*(Ptr+1) & 0xFF) == 0x8E) &&
						((*(Ptr+4) & 0xFF) == 0x20) &&
						((*(Ptr+5) & 0xFF) == 0x00) &&
						((*(Ptr+6) & 0xFF) == 0x3A) &&
						((*(Ptr+7) & 0xFF) == 0x3A) &&
						((*(Ptr+8) & 0xFF) == 0x3A) &&
						((*(Ptr+9) & 0xFF) == 0xD6) &&
						((*(Ptr+10) & 0xFF) == 0x11) &&
						((*(Ptr+11) & 0xFF) == 0x34) &&
						((*(Ptr+12) & 0xFF) == 0x04) &&
						((*(Ptr+13) & 0xFF) == 0xC6) &&
						((*(Ptr+15) & 0xFF) == 0xBD))
					{
						//
						HitType = HITTYPE_TBL_ADDR;
						HitTablePtr = Ptr+2;
						HitPagePtr = Ptr+14;
						//
						TmpStr.Format("0x%02X HitId %d",(*(Ptr-1))&0xFF,HitId);
						DebugShiftKeyMsgStrPrint(TmpStr);
					}
					HitId++;
					//
					//---------------------------------------------------------------------------------------------------------
					//---------------------------------------------------------------------------------------------------------
					//
					//             -1 +0 +1  2  3  4  5  6  7  8  9 10 11 12 13 14 15 16 17 18 19 20 21 22 23 24 25 26 27 38 29 30 31 32 33 34
					// Search for: 34 76 1F 31 EE 68 E6 C0 EF 68 20 0C 34 76 1F 31 20 06 34 76 1F 89 1F 31 3A 3A 3A D6 ww 34 04 C6 yy BD yy yy
					//
					//                             -1 +0 +1  2  3  4  5  6  7  8
					// Then Search entire ROM for: BD yy yy CE xx xx BD ww ww 00, where $wwww is address if previous line. WPC Table Address is $xxxx,zz
					if (((*(Ptr+0) & 0xFF) == 0x76) &&
						((*(Ptr+1) & 0xFF) == 0x1F) &&
						((*(Ptr+2) & 0xFF) == 0x31) &&
						((*(Ptr+3) & 0xFF) == 0xEE) &&
						((*(Ptr+4) & 0xFF) == 0x68) &&
						((*(Ptr+5) & 0xFF) == 0xE6) &&
						((*(Ptr+6) & 0xFF) == 0xC0) &&
						((*(Ptr+7) & 0xFF) == 0xEF) &&
						((*(Ptr+8) & 0xFF) == 0x68) &&
						((*(Ptr+9) & 0xFF) == 0x20) &&
						((*(Ptr+10) & 0xFF) == 0x0C) &&
						((*(Ptr+11) & 0xFF) == 0x34) &&
						((*(Ptr+12) & 0xFF) == 0x76) &&
						((*(Ptr+13) & 0xFF) == 0x1F) &&
						((*(Ptr+14) & 0xFF) == 0x31) &&
						((*(Ptr+15) & 0xFF) == 0x20) &&
						((*(Ptr+16) & 0xFF) == 0x06) &&
						((*(Ptr+17) & 0xFF) == 0x34) &&
						((*(Ptr+18) & 0xFF) == 0x76) &&
						((*(Ptr+19) & 0xFF) == 0x1F) &&
						((*(Ptr+20) & 0xFF) == 0x89) &&
						((*(Ptr+21) & 0xFF) == 0x1F) &&
						((*(Ptr+22) & 0xFF) == 0x31) &&
						((*(Ptr+23) & 0xFF) == 0x3A) &&
						((*(Ptr+24) & 0xFF) == 0x3A) &&
						((*(Ptr+25) & 0xFF) == 0x3A) &&
						((*(Ptr+26) & 0xFF) == 0xD6) &&
						((*(Ptr+28) & 0xFF) == 0x34) &&
						((*(Ptr+29) & 0xFF) == 0x04) &&
						((*(Ptr+30) & 0xFF) == 0xC6) &&
						((*(Ptr+32) & 0xFF) == 0xBD))
					{
						int FnAddr = PageByteIdx;
						LPTSTR TmpPtr;
						unsigned long TmpCnt;

						if (Page < (CommonData.TotalPages - 2))
						{
							// Fixup FnAddr to represent a WPC address in paged ROM
							FnAddr += BASE_CODE_ADDR_PAGED_ROM;
						}
						else
						{
							FnAddr += BASE_CODE_ADDR_NONPAGED_ROM;
							if (Page == (CommonData.TotalPages - 1))
							{
								// This is somewhat hard coded with knowledge that the nonbanked memory takes up the
								// last 2 banks, and if we're in the last (conceptual) page in ROM then we're actually
								// in the last half of the non-paged ROM, which means if 
								FnAddr += PAGE_LENGTH;
							}
						}
						TmpStr.Format("Special Hit Part 1, found function at WPC Addr $%04x, WPC Page 0x%02x",FnAddr,(*(Ptr+31)));
						DebugShiftKeyMsgStrPrint(TmpStr);
						//
						for (TmpCnt = 0, TmpPtr = CommonData.StartPtr; TmpCnt < CommonData.ROMSize; TmpCnt++)
						{
							switch ((*TmpPtr++) & 0xFF)
							{
								case 0xBD:
									if (((*(TmpPtr+2) & 0xFF) == 0xCE) &&
										((*(TmpPtr+5) & 0xFF) == 0xBD) &&
										((*(TmpPtr+6) & 0xFF) == ((FnAddr>>8)&0xFF)) &&
										((*(TmpPtr+7) & 0xFF) == ((FnAddr&0xFF))) &&
										((*(TmpPtr+8) & 0xFF) == 0x00))
									{
										//
										HitType = HITTYPE_TBL_ADDR;
										HitTablePtr = TmpPtr+3;
										HitPagePtr = Ptr+31;
										//
										TmpCnt = CommonData.ROMSize; // exit inner for-loop
										//
										TmpStr.Format("Special Hit Part 2, $%02x%02x,%02x",(*HitTablePtr)&0xFF,(*(HitTablePtr+1))&0xFF,(*HitPagePtr)&0xFF);
										DebugShiftKeyMsgStrPrint(TmpStr);
										//
										TmpStr.Format("0x%02X HitId %d",(*(Ptr-1))&0xFF,HitId);
										DebugShiftKeyMsgStrPrint(TmpStr);
									}
									break;
								default:
									break;
							}
						}
					}
					//HitId++;

					break;
				default :
					break;
			}
			if (HitType != HITTYPE_NONE)
			{
				if (ProcessHitType(HitType, HitTablePtr, HitPagePtr, Ptr, &FullFrameImageData.TableAddress) != 0)
				{
					TmpStr.Format("ProcessHitType() error");
					DebugShiftKeyMsgStrPrint(TmpStr);
					break;
				}
				return 0;
			}
		}
	}
	return -1;
}
int DMD::InitFonts()
{
	// Example assembly for loading font table (IJ_L7):
	//-------------------------------------------------------------------------------------------------------------------------
	// D891: BE 82 A9    LDX   $82A9            ; X gets bytes from $82A9 Font Table pointer address
	// D894: 3A          ABX                    ; 
	// D895: 58          ASLB                   ;
	// D896: 3A          ABX                    ; B was index of the font to use, so X pointed to font byte and 2 bytes that were put at $04EE
	// D897: D6 11       LDB   $11              ; B gets current ROM bank
	// D899: 34 04       PSHS  B                ; Save it
	// D89B: F6 82 AB    LDB   $82AB            ; B gets ROM bank of the font table
	// D89E: BD 8F FB    JSR   $8FFB            ; Set ROM bank to font table
	//-------------------------------------------------------------------------------------------------------------------------
	//
	// Some variations found among different ROMS:
	//
	// Search for: BE xx xx 3A 58 3A D6 yy 34 04 F6 zz zz BD ww ww, WPC Table address address is xxxx in non-banked ROM
	// Search for: BE xx xx 3A 58 3A D6 yy 34 04 BD zz zz BD ww ww, WPC Table address address is xxxx in non-banked ROM
	// Search for: BE xx xx 3A 58 3A D6 yy 34 04 BD zz zz F6 ww ww, WPC Table address address is xxxx in non-banked ROM
	// Search for: BE xx xx 3A 58 3A D6 yy 34 04 F6 zz zz F6 ww ww, WPC Table address address is xxxx in non-banked ROM
	//
	//
	// The above appears to successfully find the Font table pointer on all ROMs.
	// Following that appears to always be the Graphics table.
	// Following that appears to be the Animation table on some ROMs.
	// 
	int Page,PageByteIdx;
	LPTSTR Ptr = CommonData.StartPtr;
	LPTSTR HitTablePtr,HitPagePtr;
	int HitType;

	TmpStr.Format("Searching ROM for Master Font Table Address");
	DebugShiftKeyMsgStrPrint(TmpStr);

	for (Page = 0; Page < CommonData.TotalPages; Page++)
	{
		for (PageByteIdx = 0; PageByteIdx < PAGE_LENGTH; PageByteIdx++)
		{
			HitType = HITTYPE_NONE;
			HitTablePtr = HitPagePtr = NULL;

			switch ((*Ptr++) & 0xFF)
			{
				case 0xBE :
					//
					//             -1 +0 +1  2  3  4  5  6  7  8  9 10 11 12 13 14
					// Search for: BE xx xx 3A 58 3A D6 yy 34 04 F6 zz zz BD ww ww, WPC Table address address is xxxx in non-banked ROM
					// Search for: BE xx xx 3A 58 3A D6 yy 34 04 BD zz zz BD ww ww, WPC Table address address is xxxx in non-banked ROM
					// Search for: BE xx xx 3A 58 3A D6 yy 34 04 BD zz zz F6 ww ww, WPC Table address address is xxxx in non-banked ROM
					// Search for: BE xx xx 3A 58 3A D6 yy 34 04 F6 zz zz F6 ww ww, WPC Table address address is xxxx in non-banked ROM
					if (PageByteIdx >= (PAGE_LENGTH-16)) // don't try to read out of bounds, going to read up to 16 bytes after Ptr
					{
						break;
					}
					if (((*(Ptr+2) & 0xFF) == 0x3A) &&
						((*(Ptr+3) & 0xFF) == 0x58) &&
						((*(Ptr+4) & 0xFF) == 0x3A) &&
						((*(Ptr+5) & 0xFF) == 0xD6) &&
						((*(Ptr+7) & 0xFF) == 0x34) &&
						((*(Ptr+8) & 0xFF) == 0x04) &&
						(((*(Ptr+9) & 0xFF) == 0xF6) || ((*(Ptr+9) & 0xFF) == 0xBD)) &&
						(((*(Ptr+12) & 0xFF) == 0xBD) || ((*(Ptr+12) & 0xFF) == 0xF6)))
					{
						//
						HitType = HITTYPE_TBL_ADDR_ADDR;
						HitTablePtr = Ptr;
					}
					break;

				default :
					break;
			}
			if (HitType != HITTYPE_NONE)
			{
				if (ProcessHitType(HitType, HitTablePtr, HitPagePtr, Ptr, &VariableSizedImageData.TableAddress) != 0)
				{
					TmpStr.Format("ProcessHitType() error");
					DebugShiftKeyMsgStrPrint(TmpStr);
					break;
				}
				return 0;
			}
		}
	}
	return -1;
}
#endif // instead of looking for Graphics/Font/Animation tables separately from opcodes, just find Font table then Graphics/Animation tables usually follow

int DMD::InitTableAddrs()
{
	// Example assembly for loading font table (IJ_L7):
	//-------------------------------------------------------------------------------------------------------------------------
	// D891: BE 82 A9    LDX   $82A9            ; X gets bytes from $82A9 Font Table pointer address
	// D894: 3A          ABX                    ; 
	// D895: 58          ASLB                   ;
	// D896: 3A          ABX                    ; B was index of the font to use, so X pointed to font byte and 2 bytes that were put at $04EE
	// D897: D6 11       LDB   $11              ; B gets current ROM bank
	// D899: 34 04       PSHS  B                ; Save it
	// D89B: F6 82 AB    LDB   $82AB            ; B gets ROM bank of the font table
	// D89E: BD 8F FB    JSR   $8FFB            ; Set ROM bank to font table
	//-------------------------------------------------------------------------------------------------------------------------
	//
	// Some variations found among different ROMS:
	//
	// Search for: BE xx xx 3A 58 3A D6 yy 34 04 F6 zz zz BD ww ww, WPC Table address address is xxxx in non-banked ROM
	// Search for: BE xx xx 3A 58 3A D6 yy 34 04 BD zz zz BD ww ww, WPC Table address address is xxxx in non-banked ROM
	// Search for: BE xx xx 3A 58 3A D6 yy 34 04 BD zz zz F6 ww ww, WPC Table address address is xxxx in non-banked ROM
	// Search for: BE xx xx 3A 58 3A D6 yy 34 04 F6 zz zz F6 ww ww, WPC Table address address is xxxx in non-banked ROM
	//
	//
	// The above appears to successfully find the Font table pointer on all ROMs.
	// Following that appears to always be the Graphics table.
	// Following that appears to be the Animation table on some ROMs.
	// 
	int Page,PageByteIdx;
	LPTSTR Ptr = CommonData.StartPtr;
	LPTSTR HitTablePtr,HitPagePtr;
	unsigned long RomAddr;
	int WpcAddr;

	TmpStr.Format("Searching ROM for Master Animation Table Address");
	DebugShiftKeyMsgStrPrint(TmpStr);

	for (Page = 0; Page < CommonData.TotalPages; Page++)
	{
		for (PageByteIdx = 0; PageByteIdx < PAGE_LENGTH; PageByteIdx++)
		{
			HitTablePtr = HitPagePtr = NULL;

			switch ((*Ptr++) & 0xFF)
			{
				case 0xBE :
					//
					//             -1 +0 +1  2  3  4  5  6  7  8  9 10 11 12 13 14
					// Search for: BE xx xx 3A 58 3A D6 yy 34 04 F6 zz zz BD ww ww, WPC Table address address is xxxx in non-banked ROM
					// Search for: BE xx xx 3A 58 3A D6 yy 34 04 BD zz zz BD ww ww, WPC Table address address is xxxx in non-banked ROM
					// Search for: BE xx xx 3A 58 3A D6 yy 34 04 BD zz zz F6 ww ww, WPC Table address address is xxxx in non-banked ROM
					// Search for: BE xx xx 3A 58 3A D6 yy 34 04 F6 zz zz F6 ww ww, WPC Table address address is xxxx in non-banked ROM
					if (PageByteIdx >= (PAGE_LENGTH-16)) // don't try to read out of bounds, going to read up to 16 bytes after Ptr
					{
						break;
					}
					if (((*(Ptr+2) & 0xFF) == 0x3A) &&
						((*(Ptr+3) & 0xFF) == 0x58) &&
						((*(Ptr+4) & 0xFF) == 0x3A) &&
						((*(Ptr+5) & 0xFF) == 0xD6) &&
						((*(Ptr+7) & 0xFF) == 0x34) &&
						((*(Ptr+8) & 0xFF) == 0x04) &&
						(((*(Ptr+9) & 0xFF) == 0xF6) || ((*(Ptr+9) & 0xFF) == 0xBD)) &&
						(((*(Ptr+12) & 0xFF) == 0xBD) || ((*(Ptr+12) & 0xFF) == 0xF6)))
					{
						//
						HitTablePtr = Ptr;
						HitPagePtr = (Ptr+2); // not used by HITTYPE_TBL_ADDR_ADDR, but setting to a known value here
					
						if (GetROMAddressFromAddrOf3ByteWPCAddrPage(HitTablePtr, &RomAddr) != 0)
						{
							TmpStr.Format("Error from GetROMAddressFromAddrOf3ByteWPCAddrPage(), Passed it WPC Font Table Pointer opcode: $%02x %02x",(*HitTablePtr)&0xFF,(*(HitTablePtr+1))&0xFF);
							DebugShiftKeyMsgStrPrint(TmpStr);
							return -1;
						}

						//
						TmpStr.Format("Address in ROM of Font Table Pointer 0x%05x",RomAddr);
						DebugShiftKeyMsgStrPrint(TmpStr);

						if (dialogType == DMD_DIALOG_TYPE_FONTDATA)
						{
							if (ProcessHitType(HITTYPE_TBL_ADDR_ADDR, HitTablePtr, HitPagePtr, Ptr, &VariableSizedImageData.TableAddress) != 0)
							{
								TmpStr.Format("Error from ProcessHitType while trying to process Font Table Pointer opcode: $%02x %02x",(*HitTablePtr)&0xFF,(*(HitTablePtr+1))&0xFF);
								DebugShiftKeyMsgStrPrint(TmpStr);
								return -1;
							}
							//
							TmpStr.Format("Found Address in ROM of Font Table 0x%05x",VariableSizedImageData.TableAddress);
							DebugShiftKeyMsgStrPrint(TmpStr);
						}

						// Now re-load Font table Addr Pointer and advance to Graphic Table....
						HitTablePtr = &CommonData.StartPtr[RomAddr];
						HitPagePtr = &CommonData.StartPtr[RomAddr+2]; // in some cases when addr is in non-banked ROM this byte will get ignored
						WpcAddr = ((((*(HitTablePtr))&0xFF)<<8) + ((*(HitTablePtr+1))&0xFF))&0xFFFF;
						if (((WpcAddr >= BASE_CODE_ADDR_NONPAGED_ROM) && (WpcAddr < (BASE_CODE_ADDR_NONPAGED_ROM + NONPAGED_LENGTH))) && (((*HitPagePtr)&0xFF) != NONPAGED_BANK_INDICATOR))
						{
							RomAddr+=2;  // PagePtr will end up pointing to invalid page but it will get fixed up to 0xff
						}
						else
						{
							RomAddr+=3;
						}

						//
						TmpStr.Format("Address in ROM of Graphics Table Pointer 0x%05x",RomAddr);
						DebugShiftKeyMsgStrPrint(TmpStr);

						//
						HitTablePtr = &CommonData.StartPtr[RomAddr];
						HitPagePtr = &CommonData.StartPtr[RomAddr+2]; // in some cases when addr is in non-banked ROM this byte will get ignored

						//
						if (ProcessHitType(HITTYPE_TBL_ADDR, HitTablePtr, HitPagePtr, Ptr, &FullFrameImageData.TableAddress) != 0)
						{
							TmpStr.Format("Error from ProcessHitType while trying to process Graphic Table Pointer: $%02x %02x",(*HitTablePtr)&0xFF,(*(HitTablePtr+1))&0xFF);
							DebugShiftKeyMsgStrPrint(TmpStr);
							if (dialogType == DMD_DIALOG_TYPE_FONTDATA)
							{
								return 0; // just return, we found font addr but couldn't find graphic table, no big deal
							}
							return -1;  // looking for graphics or animation table, some problem happened, return error
						}
						//
						TmpStr.Format("Found Address in ROM of Graphics Table 0x%05x",FullFrameImageData.TableAddress);
						DebugShiftKeyMsgStrPrint(TmpStr);

						if (dialogType != DMD_DIALOG_TYPE_ANIDATA)
						{
							return 0; // found graphics table addr, no need to loop up animation table addr
						}

						// Now re-load Graphics table Addr Pointer and advance to Animation Table....
						HitTablePtr = &CommonData.StartPtr[RomAddr];
						HitPagePtr = &CommonData.StartPtr[RomAddr+2]; // in some cases when addr is in non-banked ROM this byte will get ignored
						WpcAddr = ((((*(HitTablePtr))&0xFF)<<8) + ((*(HitTablePtr+1))&0xFF))&0xFFFF;
						if (((WpcAddr >= BASE_CODE_ADDR_NONPAGED_ROM) && (WpcAddr < (BASE_CODE_ADDR_NONPAGED_ROM + NONPAGED_LENGTH))) && (((*HitPagePtr)&0xFF) != NONPAGED_BANK_INDICATOR))
						{
							RomAddr+=2;  // PagePtr will end up pointing to invalid page but it will get fixed up to 0xff
						}
						else
						{
							RomAddr+=3;
						}

						TmpStr.Format("Address in ROM of Animation Table Pointer 0x%05x",RomAddr);
						DebugShiftKeyMsgStrPrint(TmpStr);

						//
						HitTablePtr = &CommonData.StartPtr[RomAddr];
						HitPagePtr = &CommonData.StartPtr[RomAddr+2]; // in some cases when addr is in non-banked ROM this byte will get ignored

						//
						if (ProcessHitType(HITTYPE_TBL_ADDR, HitTablePtr, HitPagePtr, Ptr, &VariableSizedImageData.TableAddress) != 0)
						{
							TmpStr.Format("Error from ProcessHitType while trying to process Animation Table Pointer: $%02x %02x",(*HitTablePtr)&0xFF,(*(HitTablePtr+1))&0xFF);
							DebugShiftKeyMsgStrPrint(TmpStr);
							return -1;  // looking for animation table, some problem happened, return error
						}
						//
						TmpStr.Format("Found Address in ROM of Animation Table 0x%05x",VariableSizedImageData.TableAddress);
						DebugShiftKeyMsgStrPrint(TmpStr);

						return 0;
					}
					break;

				default :
					break;
			}
		}
	}
	return -1;
}

void DMD::CheckKeyStateForDebugFlags()
{
	// if shift is pressed, we'll show some debug messages
	debugKeyBitmask |= ((GetKeyState(VK_LSHIFT) & 0x8000) || (GetKeyState(VK_RSHIFT) & 0x8000))?DEBUG_KEY_BIT_SHIFTKEYS:0;

	// if control is pressed, we'll show some debug messages
	debugKeyBitmask |= ((GetKeyState(VK_LCONTROL) & 0x8000) || (GetKeyState(VK_RCONTROL) & 0x8000))?DEBUG_KEY_BIT_CONTROLKEYS:0;
}

int DMD::Init()
{
	memset(&CommonData,0,sizeof(CommonData));
	memset(&FullFrameImageData,0,sizeof(FullFrameImageData));
	memset(&VariableSizedImageData,0,sizeof(VariableSizedImageData));

	CheckKeyStateForDebugFlags();

	if (InitCommon() != 0)
	{
		return -1;
	}

	if (InitTableAddrs() != 0)
	{
		AfxMessageBox("Could not determine data table location in ROM image");
		return -1;
	}

	switch (dialogType)
	{
		case DMD_DIALOG_TYPE_GRAPHICS:
			//
			FullFrameImageData.CurrentImageIndex = 0;
			break;

		case DMD_DIALOG_TYPE_FONTDATA:
		case DMD_DIALOG_TYPE_ANIDATA:
			//
			if (PreAnalyzeVariableSizedImageTable() != 0)
			{
				// PreAnalyzeVariableSizedImageTable() should have printed whatever error caused it to return != 0 value
				return -1;
			}
				
			//
			VariableSizedImageData.CurrentTableIndex = VariableSizedImageData.minTableIndex;

			//
			if (GetFirstImageIndex(&VariableSizedImageData.CurrentImageIndex,VariableSizedImageData.CurrentTableIndex) != 0)
			{
				TmpStr.Format("Error setting up first image index");
				DebugControlKeyMsgStrPrint(TmpStr);
			}

			//
			if (FullFrameImageData.TableAddress != 0)
			{
				DecodeFullFrameGraphic(0); // for fun, 3rd DMD panel will just show first 2 blended graphics in the ROM
			}
			break;

		default:
			AfxMessageBox("Unexpected error, dialogType should have already been validated.");
			return -1;
	}

	//
	DecodeCurrentIndex();

	return 0;
}
void DMD::exportCurrent() {

	FILE *file;
	DWORD tick;

	DMDPlanes* pPlanes = &FullFrameImageData.Planes;
	unsigned char *Plane_0Ptr      = pPlanes->Plane0.Plane_Data;
	unsigned char *Plane_0XorFlags = pPlanes->Plane0.Plane_XorFlags;
	unsigned char *Plane_0XorBits  = pPlanes->Plane0.Plane_XorBits;
	unsigned char *Plane_0Skipped  = pPlanes->Plane0.Plane_Skipped;
	unsigned char *Plane_1Ptr      = pPlanes->Plane1.Plane_Data;
	unsigned char *Plane_1XorFlags = pPlanes->Plane1.Plane_XorFlags;
	unsigned char *Plane_1XorBits  = pPlanes->Plane1.Plane_XorBits;
	unsigned char *Plane_1Skipped  = pPlanes->Plane1.Plane_Skipped;
    unsigned char *Plane_0Previous = PreviousPlaneDataPane0;
    unsigned char *Plane_1Previous = PreviousPlaneDataPane1;
	int i,j,k;
	int RowIndex, ColumnIndex;
    ThisPixel thisPixel0;
    ThisPixel thisPixel1;
	unsigned char ReadMask;
	unsigned char PLANE_BITS;

	if( FullFrameImageData.Planes.Plane0.Plane_Status ==  PLANE_STATUS_VALID ) {
		// create a RGBA char array from both planes and encode it with LodePNG
		// then save to disk
		int w = 128; int h = 32;
		unsigned char* image = (unsigned char*)malloc( w * h );
		memset(image, 0, w*h);
		unsigned char* p = image;
		unsigned char* pSrc = FullFrameImageData.Planes.Plane0.Plane_Data;
		unsigned char* pSrc1 = FullFrameImageData.Planes.Plane1.Plane_Data;

	for (i = 0; i < DMD_ROWS; i++)
	{
		for (j = 0; j < (DMD_COLUMNS/8); j++)
		{
			for (ReadMask = 0x01, k = 0; k < 8; k++,ReadMask <<= 1)
			{
				PLANE_BITS = 0x00;
				if (*Plane_0Ptr & ReadMask)
				{
					PLANE_BITS |= PLANE0_ON;
				}
				if (*Plane_0Skipped & ReadMask)
				{
					PLANE_BITS |= PLANE0_SKIPPED;
				}
				if (*Plane_0XorFlags & ReadMask)
				{
                    if (*Plane_0XorBits & ReadMask)
                    {
					   PLANE_BITS |= PLANE0_XORED; // XOR flag <and> XOR bit then flip bit from previous display
                    }
                    else
                    {
                       PLANE_BITS |= PLANE0_SKIPPED; // XOR flag <and NOT> XOR bit, then treat it as a skip
                    }
				}
				if (*Plane_1Ptr & ReadMask)
				{
					PLANE_BITS |= PLANE1_ON;
				}
				if (*Plane_1Skipped & ReadMask)
				{
					PLANE_BITS |= PLANE1_SKIPPED;
				}
				if (*Plane_1XorFlags & ReadMask)
				{
                    if (*Plane_1XorBits & ReadMask)
                    {
					   PLANE_BITS |= PLANE1_XORED; // XOR flag <and> XOR bit then flip bit from previous display
                    }
                    else
                    {
                       PLANE_BITS |= PLANE1_SKIPPED; // XOR flag <and NOT> XOR bit, then treat it as a skip
                    }
				}

				//
				ColumnIndex = ((((j * 8) + k)) * PIXEL_WIDTH);
				RowIndex = (i * PIXEL_HEIGHT);

				//
				// Determine what color to show for medium colored plane
				//
				if (true)
				{
                    thisPixel0 = ThisPixel_Off;
					if (PLANE_BITS & PLANE0_ON)
					{
                       thisPixel0 = ThisPixel_On;
					}
					else if (PLANE_BITS & PLANE0_SKIPPED)
					{
						if (false)
						{
                           thisPixel0 = ThisPixel_Skipped;
						}
						else if (*Plane_0Previous & ReadMask)
                        {
                           thisPixel0 = ThisPixel_On;
						}
					}
					else if (PLANE_BITS & PLANE0_XORED)
					{
						if (false)
						{
                           thisPixel0 = ThisPixel_Xored;
						}
						else if (!(*Plane_0Previous & ReadMask))
                        {
                           thisPixel0 = ThisPixel_On;
						}
					}
				}
				
				RowIndex += ((DMD_ROWS + 1) * PIXEL_HEIGHT);

				//
				// Determine what color to show for dim plane
				//
				if (true)
				{
                    thisPixel1 = ThisPixel_Off;
					if (PLANE_BITS & PLANE1_ON)
					{
                       thisPixel1 = ThisPixel_On;
					}
					else if (PLANE_BITS & PLANE1_SKIPPED)
					{
						if (false)
						{
                           thisPixel1 = ThisPixel_Skipped;
						}
						else if (*Plane_1Previous & ReadMask)
						{
                           thisPixel1 = ThisPixel_On;
						}
					}
					else if (PLANE_BITS & PLANE1_XORED)
					{
						if (false)
						{
                           thisPixel1 = ThisPixel_Xored;
						}
						else if (!(*Plane_1Previous & ReadMask))
						{
                           thisPixel1 = ThisPixel_On;
						}
					}
                    
				}

                // Save "previous" frame data
                if (thisPixel0 == ThisPixel_Off)
                {
                   *Plane_0Previous &= ~ReadMask;
                }
                else if (thisPixel0 == ThisPixel_On)
                {
                   *Plane_0Previous |= ReadMask;
                }

                if (thisPixel1 == ThisPixel_Off)
                {
                   *Plane_1Previous &= ~ReadMask;
                }
                else if (thisPixel1 == ThisPixel_On)
                {
                   *Plane_1Previous |= ReadMask;
                }

				RowIndex += ((DMD_ROWS + 1) * PIXEL_HEIGHT);

				//
				// Determine what color to show for blended plane
				//
				if (true)
				{
                   if ((thisPixel0 == ThisPixel_On) && (thisPixel1 == ThisPixel_On))
                   {
 					   *p = 3;
                   }
                   else if (thisPixel0 == ThisPixel_On)
                   {
 					   *p = 2;
                   }
                   else if (thisPixel1 == ThisPixel_On)
                   {
     				   *p = 1;
                   }
                   else
                   {
     				   *p = 0;
				   }
				}
				p ++;
			} // for mask
			Plane_0Ptr++;
			Plane_1Ptr++;
			Plane_0Skipped++;
			Plane_1Skipped++;
			Plane_0XorFlags++;
			Plane_1XorFlags++;
			Plane_0XorBits++;
			Plane_1XorBits++;
            Plane_0Previous++;
            Plane_1Previous++;

		}
       
	}
	// write raw file format
	char filename[100];
	strftime(filename, sizeof(filename), "%d%m%y_%H%M%S_wpcedit_dump.raw", gmtime(&actTime));
	file = fopen(filename, "rb");
	if (file == NULL)
	{
		file = fopen(filename, "wb");
		fputc(0x52, file);
		fputc(0x41, file);
		fputc(0x57, file);
		fputc(0x00, file);
		fputc(0x01, file);
		fputc(128, file);
		fputc(32, file);
		fputc(3, file);
	} else {
		fclose(file);
		file = fopen(filename, "ab");
	}	
	tick = GetTickCount();
	fwrite(&tick, 1, 4, file);
	fwrite(PreviousPlaneDataPane1, sizeof(char), 512, file);
	fwrite(PreviousPlaneDataPane0, sizeof(char), 512, file);
	fwrite(PreviousPlaneDataPane0, sizeof(char), 512, file);
	fclose(file);

	// write pinmame txt format
	strftime(filename, sizeof(filename), "%d%m%y_%H%M%S_wpcedit_dump.txt", gmtime(&actTime));
	file = fopen(filename, "a");
	if (file) {
	  fprintf(file, "0x%08x\n", tick);
	  for (int jj = 0; jj < h; jj++) {
		  for (int ii = 0; ii < w; ii++)
		  {
			  const UINT8 col = image[jj*w + ii];
			  fprintf(file, "%01x", col);
		  }
		  fprintf(file, "\n");
	  }
	  fprintf(file, "\n");
	  fclose(file);
	}
	free((void*)image);

	}

}

void DMD::DecodeFullFrameGraphic(unsigned long GraphicIndex)
{
	DecodeImageToPlane(GraphicIndex, &FullFrameImageData.Planes.Plane0);
	DecodeImageToPlane((GraphicIndex + 1), &FullFrameImageData.Planes.Plane1);
	if( m_Export.GetCheck() ) {
		exportCurrent();
	}
}

void DMD::DecodeVariableSizedImageData()
{
	DecodeVariableSizedImageIndexToPlane(VariableSizedImageData.CurrentTableIndex, VariableSizedImageData.CurrentImageIndex, &VariableSizedImageData.Planes);

	// If error then force any stale offset values to 0
	if (VariableSizedImageData.Planes.Plane0.Plane_Status != PLANE_STATUS_VALID)
	{
		VariableSizedImageData.CurrentImageXSize = 0;
		VariableSizedImageData.CurrentImageYSize = 0;
		VariableSizedImageData.CurrentImageXShift = 0;
		VariableSizedImageData.CurrentImageYShift = 0;
	}
}

void DMD::DecodeCurrentIndex(void)
{
    // bWiped no longer needs to take precedence, if we're here it means somebody pressed Next/Previous
    bWiped = FALSE;

	switch (dialogType)
	{
		case DMD_DIALOG_TYPE_GRAPHICS:
			DecodeFullFrameGraphic(FullFrameImageData.CurrentImageIndex);
			break;

		case DMD_DIALOG_TYPE_FONTDATA:
		case DMD_DIALOG_TYPE_ANIDATA:
			DecodeVariableSizedImageData();
			break;

		default:
			break;
	}
	//
	UpdateControls();
	UpdateStaticTextBoxes();
}

int DMD::DecrementVariableSizedImageIndex(int *pTableIndex, int *pImageIndex)
{
	int tmpImageIndex;

	if ((pTableIndex == NULL) || (pImageIndex == NULL))
	{
		return -1;
	}

	//
	if (GetFirstImageIndex(&tmpImageIndex,*pTableIndex) != 0)
	{
		return -1;
	}
	
	//
	if (((*pImageIndex)&0xFF) > (tmpImageIndex&0xFF))
	{
		//
		if (GetPrevImageIndex(pImageIndex,*pTableIndex) != 0)
		{
			return -1;
		}
		return 0;
	}
	if (*pTableIndex > VariableSizedImageData.minTableIndex)
	{
		//
		*pTableIndex = (*pTableIndex) - 1;

		//
		if (GetLastImageIndex(pImageIndex,*pTableIndex) != 0)
		{
			return -1;
		}
		return 0;
	}

	// else we must be at first indexes, do nothing, just return 0, no errors.
	return 0;
}

int DMD::IncrementVariableSizedImageIndex(int *pTableIndex, int *pImageIndex)
{
	int tmpImageIndex;

	if ((pTableIndex == NULL) || (pImageIndex == NULL))
	{
		return -1;
	}

	//
	if (GetLastImageIndex(&tmpImageIndex,*pTableIndex) != 0)
	{
		return -1;
	}

	//
	if (((*pImageIndex)&0xFF) < (tmpImageIndex&0xFF))
	{
		//
		if (GetNextImageIndex(pImageIndex,*pTableIndex) != 0)
		{
			return -1;
		}
		return 0;
	}
	if (*pTableIndex < VariableSizedImageData.maxTableIndex)
	{
		//
		*pTableIndex = (*pTableIndex) + 1;

		//
		if (GetFirstImageIndex(pImageIndex,*pTableIndex) != 0)
		{
			return -1;
		}
		return 0;
	}

	// else we must be at last indexes, do nothing, just return 0, no errors.
	return 0;
}

void DMD::DecodePreviousIndex(int count)
{
    switch (dialogType)
	{
		case DMD_DIALOG_TYPE_GRAPHICS:
            while ((count--) && (FullFrameImageData.CurrentImageIndex))
			{
				FullFrameImageData.CurrentImageIndex--;
			}
			break;

		case DMD_DIALOG_TYPE_FONTDATA:
		case DMD_DIALOG_TYPE_ANIDATA:
			//
			if (VariableSizedImageData.Planes.Plane0.Plane_Status == PLANE_STATUS_VALID)
			{
				if (VariableSizedImageData.CurrentImageYShift > 0)
				{
					VariableSizedImageData.CurrentImageYShift -= (IMAGE_SHIFT_Y_PIXEL_COUNT * count);
					if (VariableSizedImageData.CurrentImageYShift < 0)
					{
						VariableSizedImageData.CurrentImageYShift = 0;
					}
					break;
				}
				if (VariableSizedImageData.CurrentImageXShift > 0)
				{
					VariableSizedImageData.CurrentImageXShift -= (IMAGE_SHIFT_X_PIXEL_COUNT * count);
					if (VariableSizedImageData.CurrentImageXShift < 0)
					{
						VariableSizedImageData.CurrentImageXShift = 0;
					}
					break;
				}
			}
			VariableSizedImageData.CurrentImageXShift = -1;
			VariableSizedImageData.CurrentImageYShift = -1;
			//
            while (count--)
            {
			   if (DecrementVariableSizedImageIndex(&VariableSizedImageData.CurrentTableIndex, &VariableSizedImageData.CurrentImageIndex) != 0)
			   {
			      //TmpStr.Format("Unexpected error decrementing image indexes");
				  //AfxMessageBox(TmpStr);
			   }
            }
			break;

		default:
			break;
	}

	//
	DecodeCurrentIndex();
	InvalidateDMDPages();
}

void DMD::DecodeNextIndex(int count)
{
	switch (dialogType)
	{
		case DMD_DIALOG_TYPE_GRAPHICS:
            while (count--)
            {
			   //if (FullFrameImageData.CurrentImageIndex < MAX_GRAPHIC_INDEX)
			   {
				   FullFrameImageData.CurrentImageIndex++;
			   }
            }
			break;

		case DMD_DIALOG_TYPE_FONTDATA:
		case DMD_DIALOG_TYPE_ANIDATA:
			//
			if (VariableSizedImageData.Planes.Plane0.Plane_Status == PLANE_STATUS_VALID)
			{
				if ((VariableSizedImageData.CurrentImageXShift + DMD_COLUMNS) < VariableSizedImageData.CurrentImageXSize)
				{
					VariableSizedImageData.CurrentImageXShift += (IMAGE_SHIFT_X_PIXEL_COUNT * count);
					break;
				}
				if ((VariableSizedImageData.CurrentImageYShift + DMD_ROWS) < VariableSizedImageData.CurrentImageYSize)
				{
					VariableSizedImageData.CurrentImageYShift += (IMAGE_SHIFT_Y_PIXEL_COUNT * count);
					break;
				}
			}
			VariableSizedImageData.CurrentImageXShift = 0;
			VariableSizedImageData.CurrentImageYShift = 0;
			//
            while (count--)
            {
			   if (IncrementVariableSizedImageIndex(&VariableSizedImageData.CurrentTableIndex, &VariableSizedImageData.CurrentImageIndex) != 0)
			   {
				   //TmpStr.Format("Unexpected error advancing image indexes");
				   //AfxMessageBox(TmpStr);
			   }
			}
			break;

		default:
			break;
	}

	//
	DecodeCurrentIndex();
	InvalidateDMDPages();
}

void DMD::DecodePlaneInit(DMDPlane *pPlane)
{
	//
	// We'll clear out the page of data bytes here..
	//
	memset(pPlane, 0, sizeof(DMDPlane));

	//
	// Assume the image will be valid unless otherwise determined
	//
	pPlane->Plane_Status = PLANE_STATUS_VALID;
}

void DMD::DecodeVariableSizedImageIndexToPlane(int TableIndex, int ImageIndex, DMDPlanes *pPlanes)
{
	unsigned char *DataPtr;
	unsigned long Addr;

	//
	DecodePlaneInit(&pPlanes->Plane0);
	DecodePlaneInit(&pPlanes->Plane1);

	//
	VariableSizedImageData.CurrentImageXSize = 0;
	VariableSizedImageData.CurrentImageYSize = 0;

	if (GetROMAddressOfVariableSizedImageIndex(&Addr, TableIndex, ImageIndex) != 0)
	{
		pPlanes->Plane0.Plane_Status = PLANE_STATUS_BADDIMENSION;
		pPlanes->Plane1.Plane_Status = PLANE_STATUS_BADDIMENSION;
		return;
	}

	DataPtr = (unsigned char *)&CommonData.StartPtr[Addr];
	DecodeVariableSizedImage(&DataPtr, pPlanes, TableIndex);
}

void DMD::DecodeVariableSizedImage(unsigned char **Source, DMDPlanes *pPlanes, int TableIndex)
{
	int TableHeight;
	int TableSpacing;

	unsigned char ch = **Source;

	if (GetVariableSizedImageTableMetadata(TableIndex, &TableHeight, &TableSpacing) != 0)
	{
		TmpStr.Format("Unexpected problem looking up TableIndex %d height & spacing",TableIndex);
		DebugControlKeyMsgStrPrint(TmpStr);
		return;
	}

	if ((ch > 0) && (ch <= DMD_COLUMNS))
	{
		DecodeVariableSizedImageIndex_NoHeader(Source, pPlanes, TableHeight);
	}
	else
	{
		switch (ch)
		{
			case IMAGE_CODE_MONOCHROME :         // 0x00, Typical header
			case IMAGE_CODE_BICOLOR_INDIRECT:    // Special header, bi-color image with pointer to other plane (IJ)
			case IMAGE_CODE_BICOLOR_DIRECT:      // Special header, bi-color image with other plane included
			case IMAGE_CODE_FD:                  // Unusre, but draws fine with 0x00 header processing (possibly inversed paint?)
				break;
			default:
				TmpStr.Format("Unrecognized Header Byte 0x%02x",ch);
				DebugControlKeyMsgStrPrint(TmpStr);
				break;
		}
		DecodeVariableSizedImageIndex_Header(Source, pPlanes, TableHeight, TableIndex);
	}
}

unsigned char DMD::DecodeVariableSizedImage_Centered(unsigned char **SourcePtr, unsigned char **DestPtr, int ImageHeight, int ImageWidth)
{
	unsigned char ch;
	unsigned int WriteCounter = 0;
	int i,j;

    if ((*SourcePtr) >= CommonData.EndPtr)
    {
       return PLANE_STATUS_IMAGEOUTOFRANGE;
    }

	//
	if (VariableSizedImageData.CurrentImageYShift == -1)
	{
		VariableSizedImageData.CurrentImageYShift = 0;
		while ((DMD_ROWS + VariableSizedImageData.CurrentImageYShift) < ImageHeight)
		{
			VariableSizedImageData.CurrentImageYShift += IMAGE_SHIFT_Y_PIXEL_COUNT;
		}
	}
	//
	if (VariableSizedImageData.CurrentImageXShift == -1)
	{
		VariableSizedImageData.CurrentImageXShift = 0;
		while ((DMD_COLUMNS + VariableSizedImageData.CurrentImageXShift) < ImageWidth)
		{
			VariableSizedImageData.CurrentImageXShift += IMAGE_SHIFT_X_PIXEL_COUNT;
		}
	}

	// Soak up SourcePtr bytes to account for Y shift
	for (i = 0; i < VariableSizedImageData.CurrentImageYShift; i++)
	{
		// Now write actual image pixel bytes
		for (j = 0; j < ((ImageWidth + 7) / 8); j++)
		{
			(*SourcePtr)++;
            if ((*SourcePtr) >= CommonData.EndPtr)
            {
               return PLANE_STATUS_IMAGEOUTOFRANGE;
            }
		}
	}

	//
	for (i = 0; ((i < DMD_ROWS) && (WriteCounter < DMD_PAGE_BYTES)); i++)
	{
		// Fill in header bytes to center image vertically
		if (ImageHeight < DMD_ROWS)
		{
			if ((i < ((DMD_ROWS - ImageHeight) / 2)) ||
				(i >= (((DMD_ROWS - ImageHeight) / 2) + ImageHeight)))
			{
				for (j = 0; j < (DMD_COLUMNS/8); j++)
				{
					WriteNext8BitValue(DestPtr, &WriteCounter, 0x00, WRITE_TYPE_ROWS);
				}
				continue;
			}
		}
		// Fill in empty rows if vertical shift moved tall image up but now has empty rows after the image
		if (ImageHeight > DMD_ROWS)
		{
			if (i >= (ImageHeight - VariableSizedImageData.CurrentImageYShift))
			{
				for (j = 0; j < (DMD_COLUMNS/8); j++)
				{
					WriteNext8BitValue(DestPtr, &WriteCounter, 0x00, WRITE_TYPE_ROWS);
				}
				continue;
			}
		}


		// At line that will contain image data fill in left columns to center image horizontally
		if (ImageWidth < DMD_COLUMNS)
		{
			for (j = 0; j < (((DMD_COLUMNS - ImageWidth) / 2) / 8); j++)
			{
				WriteNext8BitValue(DestPtr, &WriteCounter, 0x00, WRITE_TYPE_ROWS);
			}
		}

		// Now write actual image pixel bytes
		for (j = 0; j < ((ImageWidth + 7) / 8); j++)
		{
			ch = **SourcePtr;
			(*SourcePtr)++;
            if ((*SourcePtr) >= CommonData.EndPtr)
            {
               return PLANE_STATUS_IMAGEOUTOFRANGE;
            }
			if ((j >= ((VariableSizedImageData.CurrentImageXShift+7)/8)) && (j < (((DMD_COLUMNS+VariableSizedImageData.CurrentImageXShift)+7)/8)))
			{
				WriteNext8BitValue(DestPtr, &WriteCounter, ch, WRITE_TYPE_ROWS);
			}
		}


		// And finish writing bytes for this row
		if (ImageWidth < DMD_COLUMNS)
		{
			for (j = ((((DMD_COLUMNS - ImageWidth) / 2) / 8) + ((ImageWidth + 7) / 8)); j < (DMD_COLUMNS/8); j++)
			{
				WriteNext8BitValue(DestPtr, &WriteCounter, 0x00, WRITE_TYPE_ROWS);
			}
		}
	}

	// Soak up SourcePtr bytes to finish reading entire bitmap for oversized images that use 0xFF encoding, $SourcePtr will be sitting at next plane
	for (i = 0; i < (ImageHeight - (DMD_ROWS + VariableSizedImageData.CurrentImageYShift)); i++)
	{
		// Now write actual image pixel bytes
		for (j = 0; j < ((ImageWidth + 7) / 8); j++)
		{
			(*SourcePtr)++;
            if ((*SourcePtr) >= CommonData.EndPtr)
            {
               return PLANE_STATUS_IMAGEOUTOFRANGE;
            }
		}
	}

	//
	VariableSizedImageData.CurrentImageXSize = ImageWidth;
	VariableSizedImageData.CurrentImageYSize = ImageHeight;

	return PLANE_STATUS_VALID;
}

void DMD::DecodeVariableSizedImageIndex_NoHeader(unsigned char **SourcePtr, DMDPlanes *pPlanes, int TableHeight)
{
	unsigned char *DestPlane0 = pPlanes->Plane0.Plane_Data;
	unsigned char *DestPlane1 = pPlanes->Plane1.Plane_Data;
	unsigned char ImageWidth;

	//
	pPlanes->Plane0.Plane_Status = PLANE_STATUS_INVALID;
	pPlanes->Plane1.Plane_Status = PLANE_STATUS_INVALID;

	// Note, ->Plane_Size not shown for VariableSizedImageData display.
	pPlanes->Plane0.Plane_Size = 0;
	pPlanes->Plane0.Plane_Size = 0;

	//
	ImageWidth = **SourcePtr;
	(*SourcePtr)++;
    if ((*SourcePtr) >= CommonData.EndPtr)
    {
       return;
    }

	//
	//TmpStr.Format("DecodeVariableSizedImageIndex_NoHeader(), TableHeight 0x%02x, ImageWidth x%02x",TableHeight,ImageWidth);
	//DebugControlKeyMsgStrPrint(TmpStr);

	pPlanes->Plane0.Plane_Status = DecodeVariableSizedImage_Centered(SourcePtr, &DestPlane0, TableHeight, ImageWidth);
}

void DMD::DecodeVariableSizedImageIndex_Header(unsigned char **SourcePtr, DMDPlanes *pPlanes, int TableHeight, int TableIndex)
{
	unsigned char *DestPlane0 = pPlanes->Plane0.Plane_Data;
	unsigned char *DestPlane1 = pPlanes->Plane1.Plane_Data;
	unsigned char HeaderByte;
	unsigned char VerticalOffset;
	unsigned char HorizontalOffset;
	unsigned char ImageHeight;
	unsigned char ImageWidth;

	//
	pPlanes->Plane0.Plane_Status = PLANE_STATUS_INVALID;
	pPlanes->Plane1.Plane_Status = PLANE_STATUS_INVALID;

	// Note, ->Plane_Size not shown for VariableSizedImageData display.
	pPlanes->Plane0.Plane_Size = 0;
	pPlanes->Plane0.Plane_Size = 0;

	//
	HeaderByte = **SourcePtr;
	(*SourcePtr)++;
    if ((*SourcePtr) >= CommonData.EndPtr)
    {
       return;
    }
	VerticalOffset = **SourcePtr;
	(*SourcePtr)++;
    if ((*SourcePtr) >= CommonData.EndPtr)
    {
       return;
    }
	HorizontalOffset = **SourcePtr;
	(*SourcePtr)++;
    if ((*SourcePtr) >= CommonData.EndPtr)
    {
       return;
    }
	ImageHeight = **SourcePtr;
	(*SourcePtr)++;
    if ((*SourcePtr) >= CommonData.EndPtr)
    {
       return;
    }
	ImageWidth = **SourcePtr;
	(*SourcePtr)++;
    if ((*SourcePtr) >= CommonData.EndPtr)
    {
       return;
    }

	//TmpStr.Format("DecodeVariableSizedImageIndex_Header(), HeaderByte 0x%02x, TableHeight 0x%02x, VertOffset 0x%02x, HorizOffset 0x%02x, ImageHeight 0x%02x, ImageWidth 0x%02x",
	//	           HeaderByte, TableHeight, VerticalOffset, HorizontalOffset, ImageHeight, ImageWidth);
	//DebugControlKeyMsgStrPrint(TmpStr);

	//
	switch (HeaderByte)
	{
		case IMAGE_CODE_BICOLOR_DIRECT:
			pPlanes->Plane1.Plane_Status = DecodeVariableSizedImage_Centered(SourcePtr, &DestPlane1, ImageHeight, ImageWidth);
			pPlanes->Plane0.Plane_Status = DecodeVariableSizedImage_Centered(SourcePtr, &DestPlane0, ImageHeight, ImageWidth);
			break;

		case IMAGE_CODE_BICOLOR_INDIRECT:
			{
				int Page;
				char TmpBuf[3];
				unsigned long Addr;
				unsigned char *pBiColor;

				if (ExtractWPCAddrAndPageOfImageTable(NULL, &Page, TableIndex) != 0)
				{
					TmpStr.Format("DecodeVariableSizedImageIndex_Header(), Unexpected problem looking up TableIndex %d WPC Page",TableIndex);
					DebugControlKeyMsgStrPrint(TmpStr);
					return;
				}

				TmpBuf[0] = (**SourcePtr)&0xFF;
				(*SourcePtr)++;
                if ((*SourcePtr) >= CommonData.EndPtr)
                {
                   return;
                }
				TmpBuf[1] = (**SourcePtr)&0xFF;
				(*SourcePtr)++;
                if ((*SourcePtr) >= CommonData.EndPtr)
                {
                   return;
                }
				TmpBuf[2] = (Page&0xFF);

				if (GetROMAddressFromAddrOf3ByteWPCAddrPage(TmpBuf, &Addr) != 0)
				{
					TmpStr.Format("DecodeVariableSizedImageIndex_Header(), Unexpected problem looking up ROM address of bi-color plane from 3-byte WPC Addr 0x%02x 0x%02x 0x%02x",(TmpBuf[0]&0xFF),(TmpBuf[1]&0xFF),(TmpBuf[2]&0xFF));
					DebugControlKeyMsgStrPrint(TmpStr);
					return;
				}

				pBiColor = (unsigned char *)&CommonData.StartPtr[Addr];

				//
				pPlanes->Plane1.Plane_Status = DecodeVariableSizedImage_Centered(&pBiColor, &DestPlane1, ImageHeight, ImageWidth);
				pPlanes->Plane0.Plane_Status = DecodeVariableSizedImage_Centered(SourcePtr, &DestPlane0, ImageHeight, ImageWidth);
			}
			break;

		case IMAGE_CODE_FD:
		default:
			pPlanes->Plane0.Plane_Status = DecodeVariableSizedImage_Centered(SourcePtr, &DestPlane0, ImageHeight, ImageWidth);
			break;
	}
}

void DMD::DecodeImageToPlane(int Index, DMDPlane *pPlane)
{
	unsigned char *OriginalDataPtr;
	unsigned char *DataPtr;
	unsigned long Addr;

	//TmpStr.Format("Graphic Index %d Plane %d",Index,Plane);
	//DebugShiftKeyMsgStrPrint(TmpStr);

	//
	DecodePlaneInit(pPlane);

	// Each graphic table entry is 3 bytes long
	Addr = FullFrameImageData.TableAddress + (Index * 3);

	if (Addr >= CommonData.ROMSize)
	{
		pPlane->Plane_Status = PLANE_STATUS_TABLEENTRYOUTOFRANGE;
		return;
	}

	if (GetROMAddressFromAddrOf3ByteWPCAddrPage(&CommonData.StartPtr[Addr], &Addr) != 0)
	{
		TmpStr.Format("DecodeImageToPlane() got error from GetROMAddressFromAddrOf3ByteWPCAddrPage()");
		DebugShiftKeyMsgStrPrint(TmpStr);
		pPlane->Plane_Status = PLANE_STATUS_TABLEENTRYOUTOFRANGE;
		return;
	}

	if (Addr >= CommonData.ROMSize)
    {
        pPlane->Plane_Status = PLANE_STATUS_TABLEENTRYOUTOFRANGE;
        return;
    }

	OriginalDataPtr = DataPtr = (unsigned char *)&CommonData.StartPtr[Addr];
	pPlane->Plane_Status = DecodeFullFrameGraphicImage(&DataPtr, pPlane);
	pPlane->Plane_Size = (DataPtr - OriginalDataPtr);
}

unsigned char DMD::DecodeFullFrameGraphicImage(unsigned char **Source, DMDPlane *pPlane)
{
	unsigned char *Dest = pPlane->Plane_Data;
	unsigned char *Skipped = pPlane->Plane_Skipped;
	unsigned char *XorFlags = pPlane->Plane_XorFlags;
	unsigned char *XorBits = pPlane->Plane_XorBits;

	unsigned char ch = **Source;
	(*Source)++;
    if ((*Source) >= CommonData.EndPtr)
    {
        return PLANE_STATUS_IMAGEOUTOFRANGE;
    }

	//
	TmpStr.Format("Type 0x%02x",ch);
	DebugShiftKeyMsgStrPrint(TmpStr);

	switch (ch&0x0F)
	{
		case 0x00	:  //  Raw 32 bytes by 16 byes copy, no encodings.
			Decode_00(Source, Dest);
			break;
		case 0x01   :  //  Simple Repeats, Columns
			Decode_01(Source, Dest);
			break;
		case 0x02   :  //  Simple Repeats, Rows
			Decode_02(Source, Dest);
			break;
		case 0x03   :  //  <unsure>
			Decode_03(Source, Dest);
			return PLANE_STATUS_UNIMPLEMENTED_TYPE; // this is a cheat but we know that type 03 is not being decoded
		case 0x04   :  //  Complex Repeats, 9-byte header, Columns
			Decode_04(Source, Dest);
			break;
		case 0x05   :  //  Complex Repeats, 9-byte header, Rows
			Decode_05(Source, Dest);
			break;
		case 0x06   :  //  XOR-Repeat, Columns
			Decode_06(Source, Dest, XorFlags, XorBits);
			break;
		case 0x07   :  //  XOR-Repeat, Rows
			Decode_07(Source, Dest, XorFlags, XorBits);
			break;
		case 0x08   :  //  Bulk Skips and Bulk Repeats, Columns
			Decode_08(Source, Dest, Skipped);
			break;
		case 0x09   :  //  Bulk Skips and Bulk Repeats, Rows
			Decode_09(Source, Dest, Skipped);
			break;
		case 0x0A   :  //  Write Data Bytes or Multiple Skips, Columns
			Decode_0A(Source, Dest, Skipped);
			break;
		case 0x0B   :  //  Write Data Bytes or Multiple Skips, Rows
			Decode_0B(Source, Dest, Skipped);
			break;
		default	:
			TmpStr.Format("Unknown Image Type 0x%02x",ch);
			DebugShiftKeyMsgStrPrint(TmpStr);
			return PLANE_STATUS_UNKNOWN_TYPE;
	}

    if ((*Source) >= CommonData.EndPtr)
    {
        return PLANE_STATUS_IMAGEOUTOFRANGE;
    }

	return PLANE_STATUS_VALID;
}

//  Raw 32 bytes by 16 byes copy, no encodings.
void DMD::Decode_00(unsigned char **Source, unsigned char *Dest)
{
	int i;
	for (i = 0; i < DMD_PAGE_BYTES; i++)
	{
		*Dest++ = **Source;
		(*Source)++;
        if ((*Source) >= CommonData.EndPtr)
        {
           return;
        }
	}
}

//  Simple Repeats, Columns
void DMD::Decode_01(unsigned char **Source, unsigned char *Dest)
{
// IMAGE TYPE 0x04 or 0x01                ; EDF1h   Byte1 = Byte AFTER the 0x04
//
// Simple Repeats, Columns
//
// Format:
//  0x02                   Image type byte, byte that got us this far.
//   <Special Flag Byte>   Special 8-bit value that is used to signal repeats
//   <data starts here>
//
// This is a simple encoding very similar to IMAGE TYPE 0x05 or 0x02.  This
// encoding uses a simple single-special-byte at the top and whenever this
// byte is encountered, the following 2 bytes are used for Repeat/Data so that
// the Data is repeated for the number of times in 'Repeat'.
//
// The only difference between this and IMAGE TYPE 0x05 or 0x02 is that this
// encoding method writes in columns from LEFT to RIGHT starting at the top
// left and ending at the bottom right of the DMD.
//
	Decode_01or02(Source,&Dest,WRITE_TYPE_COLUMNS);
}

void DMD::Decode_02(unsigned char **Source, unsigned char *Dest)
{
// IMAGE TYPE 0x05 or 0x02                ; EE70h
//
// Simple Repeats, Rows
//
// Format:
//  0x02                   Image type byte, byte that got us this far.
//   <Special Flag Byte>   Special 8-bit value that is used to signal repeats
//   <data starts here>
//
// This is a very basic encoding that allows for repeats 8-bit patterns that
// might occur frequently.  This writes the DMD from the TOP to the BOTTOM,
// starting at the top left and ending at the bottom right.  As with all
// encodings, the data actually appears in reverse at every 8-bit column on the
// DMD, for example if the first 2 data bytes are A0B0, the top row, left side
// of the DMD will illuminate the pixels like: .....0.0 ....00.0
// (0 is on pixel, . is off pixel)
//
// The bytes are read from the data and written to the DMD memory (again, in
// ROWS on the DMD from top to bottom).  When a byte is found that matches the
// byte defined as <Special Flag Byte> then instead of writing the byte to the
// DMD, the following 2 bytes are read, making up the following format:
//
// <Special Flag Byte> <Length> <Pattern>
//
// The 8-bits defined in <Pattern> are written to the DMD for the number of times
// defined in <Length>.
//
// If the actual byte defined in <Special Flag Byte> needs to be drawn on the DMD
// then a <Length> byte of 1 can be used with the <Pattern> byte matching the
// <Special Flag Byte>.  The length should not be 0, if the length is zero, then
// the pattern will end up being repeated 256 times.
//
	Decode_01or02(Source,&Dest,WRITE_TYPE_ROWS);
}


void DMD::Decode_01or02(unsigned char **SourcePtr, unsigned char **DestPtr, unsigned char Type)
{
	unsigned char ch;
	unsigned char SpecialFlagByte;
	unsigned int WriteCounter;

	SpecialFlagByte = **SourcePtr;
	(*SourcePtr)++;
    if ((*SourcePtr) >= CommonData.EndPtr)
    {
       return;
    }
	WriteCounter = 0;         // Stores bytes we've written to DMD Ram
	do
	{
		ch = **SourcePtr;
		(*SourcePtr)++;
        if ((*SourcePtr) >= CommonData.EndPtr)
        {
           return;
        }
		if (ch == SpecialFlagByte)
		{
			unsigned char Value1 = **SourcePtr;
			(*SourcePtr)++;
            if ((*SourcePtr) >= CommonData.EndPtr)
            {
               return;
            }
			unsigned int Value2 = **SourcePtr;
			(*SourcePtr)++;
            if ((*SourcePtr) >= CommonData.EndPtr)
            {
               return;
            }
			do
			{
				WriteNext8BitValue(DestPtr,&WriteCounter, Value2, Type);
			} while ((--Value1) && (WriteCounter < DMD_PAGE_BYTES));
		}
		else
		{
			WriteNext8BitValue(DestPtr,&WriteCounter, ch, Type);
		}
	} while (WriteCounter < DMD_PAGE_BYTES);
}

//  <unsure>
void DMD::Decode_03(unsigned char **Source, unsigned char *Dest)
{
//	AfxMessageBox("Image type 03 not implemented");
}

void DMD::Decode_04(unsigned char **Source, unsigned char *Dest)
{
//  IMAGE TYPE 0x07 or 0x04      ; Byte1 = byte AFTER bitmap type
//
// Complex Repeats, 9-byte header, Columns
//
// Format:
//  0x04                   Image type byte, byte that got us this far.
//   <Special Flag Byte>   Special 8-bit value that is used to signal special encodings.
//   <Special Byte 1>      Special #1  Can be used for repeat counts or for actual bitmap data.
//   <Special Byte 2>      Special #2  Can be used for repeat counts or for actual bitmap data.
//   <Special Byte 3>      Special #3  Can be used for repeat counts or for actual bitmap data.
//   <Special Byte 4>      Special #4  Can be used for repeat counts or for actual bitmap data.
//   <Special Byte 5>      Special #5  Can be used for repeat counts or for actual bitmap data.
//   <Special Byte 6>      Special #6  Can be used for repeat counts or for actual bitmap data.
//   <Special Byte 7>      Special #7  Can be used for repeat counts or for actual bitmap data.
//   <Special Byte 8>      Special #8  Can be used for repeat counts or for actual bitmap data.
//    <data starts here>
//
//   All bits drawn on the dot matrix display for this image type are drawn
//   in COLUMNS starting at the top of the left most 8-bit column and ending
//   at the bottom of the right-most 8-bit column.  It should be noted that the
//   bits are also mirror-reversed for every of the 16 8-bit columns.  For
//   example when the first byte of display memory contains a value of 0xC0 the
//   top left corner of the dot matrix display will show ......OO where 'O' is
//   an illuminated pixel and '.' is an off pixel.
//
//   Data Format:  Continuous stream of bits, starting at 0x80 bit of the first
//                 byte and continuing until all 32x128 dots are accounted for.
//                 This continuous stream of bits opeates in the following
//                 manner...
//
//   When '0' bit is encountered, the following 8 bits are drawn on the dot
//   matrix directly (no special encoding).  When '1' extension bit is
//   encountered, the number of continuous 1s that follow is counted up
//   (until a zero trailing bit is encountered and consumed).  Note that the
//   maximum number of continuous 1s to follow the extension bit is 7, this
//   means there is NO trailing 0 bit that is consumed after 7 continuous 1s.
//   After 7 continuous 1s after the extension bit, the next command is
//   processed (ie if 0 then draw next 8 bits, if 1 process another extension
//   bit set).  The number of continuous 1s that follow the extension bit
//   cause the following to occur...
//
//   # of 1s following extension bit                    Effect
//   ----------------------------------------------------------------------------
//                0                      Draw 8 bits defined in <Special Byte 1>, or special repeat encoding, see below,
//                1                      Draw 8 bits defined in <Special Byte 2>, or special repeat encoding, see below,
//                2                      Draw 8 bits defined in <Special Byte 3>, or special repeat encoding, see below,
//                3                      Draw 8 bits defined in <Special Byte 4>, or special repeat encoding, see below,
//                4                      Draw 8 bits defined in <Special Byte 5>, or special repeat encoding, see below,
//                5                      Draw 8 bits defined in <Special Byte 6>, or special repeat encoding, see below,
//                6                      Draw 8 bits defined in <Special Byte 7>, or special repeat encoding, see below,
//                7                      Draw 8 bits defined in <Special Byte 8>, or special repeat encoding, see below,
//
//   <special repeat encoding>
//   If the <Special Byte X> byte matches the 8-bit value <Special Flag Byte>
//   (at top of graphic header) then those 8-bits defined in the special byte
//   will NOT be drawn, instead the bit stream is read for the next TWO VALUES.
//   The next two values that are pulled from the bit stream can be encoded by
//   referencing the Special Byte (using extension bit followed by appropriate
//   number of continuous 1s) or the next two values can be pulled from the bit
//   stream using non-extended method (a 0-bit followed by 8 bits representing
//   the value.  The next 2 values that are pulled from the bit stream can also
//   be encoded using any combination of the previously mentioned encoded
//   methods.  Typically the first of the 2 values is encoded using the
//   extension-bit method and usually the 2nd of the 2 values is also encoded
//   using the extension bit method, although it is not uncommon to see the
//   2nd of the 2 values be a direct encoded value (0 bit followed by the
//   desired 8-bit value.
//
//   The next 2 values that follow are used in the following manner:
//     <Value1>  This is the first value read after the Special Flag Byte match occurs.
//     <Value2>  This is the second value read after the Special Flag Byte match occurs.
//
//   The 8-bit value defined by <Value2> is repeated for the number of times
//   defined by <Value1>.
//
//
//struct ImageHeader
//{
//	unsigned char SpecialFlagByte;
//	unsigned char RepeatBytes[8];
//	unsigned char ReadMask;
//};
	Decode_04or05(Source, &Dest, WRITE_TYPE_COLUMNS);
}

void DMD::Decode_05(unsigned char **Source, unsigned char *Dest)
{
// Complex Repeats, 9-byte header, Rows
//
// Format:
//  0x04                   Image type byte, byte that got us this far.
//   <Special Flag Byte>   Special 8-bit value that is used to signal special encodings.
//   <Special Byte 1>      Special #1  Can be used for repeat counts or for actual bitmap data.
//   <Special Byte 2>      Special #2  Can be used for repeat counts or for actual bitmap data.
//   <Special Byte 3>      Special #3  Can be used for repeat counts or for actual bitmap data.
//   <Special Byte 4>      Special #4  Can be used for repeat counts or for actual bitmap data.
//   <Special Byte 5>      Special #5  Can be used for repeat counts or for actual bitmap data.
//   <Special Byte 6>      Special #6  Can be used for repeat counts or for actual bitmap data.
//   <Special Byte 7>      Special #7  Can be used for repeat counts or for actual bitmap data.
//   <Special Byte 8>      Special #8  Can be used for repeat counts or for actual bitmap data.
//    <data starts here>
//
// This is exactly the same as IMAGE TYPE 0x07 or 0x04 except data is written
// on the DMD ram in ROWS from top-left to bottom-right.  This takes less code
// space because there is no special code to decrement DMD ram to get the pointer
// to the top of the next column.  See image type 0x07 or 0x04 below for details.
//
	Decode_04or05(Source, &Dest, WRITE_TYPE_ROWS);
}

void DMD::Decode_04or05(unsigned char **SourcePtr, unsigned char **DestPtr, unsigned char Type)
{
	ImageHeader Header;
	unsigned char ch;
	int i;
	unsigned int WriteCounter;

	Header.ReadMask = 0x80;
	WriteCounter = 0;         // Stores bytes we've written to DMD Ram

	Header.SpecialFlagByte = **SourcePtr;
	(*SourcePtr)++;
    if ((*SourcePtr) >= CommonData.EndPtr)
    {
       return;
    }
	for (i = 0; i < 8; i++)
	{
		Header.RepeatBytes[i] = **SourcePtr;
		(*SourcePtr)++;
        if ((*SourcePtr) >= CommonData.EndPtr)
        {
           return;
        }
	}

	do
	{
		ch = ReadNext8BitValue(&Header,SourcePtr);
        if ((*SourcePtr) >= CommonData.EndPtr)
        {
           return;
        }
		if (ch == Header.SpecialFlagByte)
		{
			unsigned char Value1 = ReadNext8BitValue(&Header,SourcePtr);
            if ((*SourcePtr) >= CommonData.EndPtr)
            {
               return;
            }
			unsigned int Value2 = (unsigned int)ReadNext8BitValue(&Header,SourcePtr);
            if ((*SourcePtr) >= CommonData.EndPtr)
            {
               return;
            }
			do
			{
				WriteNext8BitValue(DestPtr,&WriteCounter, Value2, Type);
			} while ((--Value1) && (WriteCounter < DMD_PAGE_BYTES));
		}
		else
		{
			WriteNext8BitValue(DestPtr,&WriteCounter, ch, Type);
		}
	} while (WriteCounter < DMD_PAGE_BYTES);
	if (Header.ReadMask == 0x80)
	{
		(*SourcePtr)--;
	}
}

void DMD::WriteNext8BitValue(unsigned char **DestPtr, unsigned int *WriteCounterPtr, unsigned char ch, unsigned char Type)
{
	(**DestPtr) = ch;      // Write the actual 8-bit value
	if (((*WriteCounterPtr)++) >= DMD_PAGE_BYTES)
	{
		return;
	}

	if (Type == WRITE_TYPE_ROWS)
	{
		(*DestPtr)++;
		return;
	}
	if (!((*WriteCounterPtr) % DMD_ROWS))
	{
		// 
		// We just finished writing 32 bytes for a particular column.
		// We need to Adjust the write pointer to point up to the top
		// of the next column over.
		//
		(*DestPtr) -= (((DMD_COLUMNS/8) * (DMD_ROWS - 2)) + ((DMD_COLUMNS/8) - 1));
	}
	else
	{
		//
		// We just finished writing some byte within the 32-byte column
		// NOT the last row of the column, so just advance to next row down
		// within this column.
		//
		(*DestPtr) += (DMD_COLUMNS/8);
	}
}

unsigned char DMD::ReadNext8BitValue(struct ImageHeader *Header, unsigned char **SourcePtr)
{
	unsigned char ch = ReadNextBit(Header, SourcePtr);
    if ((*SourcePtr) >= CommonData.EndPtr)
    {
       return 0x00;
    }
	unsigned char WriteMask;
	unsigned char ReturnValue;
	int i;

	if (ch)
	{
		int OnesCount = 0;
		for (i = 0; i < 7; i++) // at most 7 one-bits to follow
		{
			if (ReadNextBit(Header, SourcePtr))
			{
				OnesCount++;
			}
			else
			{
				i = 7;
			}
            if ((*SourcePtr) >= CommonData.EndPtr)
            {
                return 0x00;
            }
		}
		ReturnValue = Header->RepeatBytes[OnesCount];
	}
	else
	{
		// 
		// Read the next 8 bits and return the value.
		//
		WriteMask = 0x80;
		ReturnValue = 0x00;
		for (i = 0; i < 8; i++)
		{
			if (ReadNextBit(Header, SourcePtr))
			{
				ReturnValue |= WriteMask;
			}
            if ((*SourcePtr) >= CommonData.EndPtr)
            {
                return 0x00;
            }
			WriteMask >>= 1;
		}
	}
	return (ReturnValue);
}

unsigned char DMD::ReadNextBit(struct ImageHeader *Header, unsigned char **SourcePtr)
{
	unsigned char ch = (**SourcePtr & Header->ReadMask);
	if (!(Header->ReadMask >>= 1))
	{
		Header->ReadMask = 0x80;
		(*SourcePtr)++;
        if ((*SourcePtr) >= CommonData.EndPtr)
        {
            return 0x00;
        }
	}
	return ch;
}


void DMD::Decode_06(unsigned char **Source, unsigned char *Dest, unsigned char *XorFlags, unsigned char *XorBits)
{
// IMAGE TYPE 0x09 or 0x06                ; ECE6h
//
// XOR-Repeat, Columns
//
// Format:
//  0x02                   Image type byte, byte that got us this far.
//   <Special Flag Byte>   Special 8-bit value that is used to signal repeats
//   <data starts here>
//
// This encoding is identical to IMAGE TYPE 0x0A or 0x07 except the data is
// drawn to DMD ram in COLUMNS from LEFT to RIGHT starting at the top left of
// the DMD and ending at the bottom right.
//
	Decode_06or07(Source, &Dest, &XorFlags, &XorBits, WRITE_TYPE_COLUMNS);
}

void DMD::Decode_07(unsigned char **Source, unsigned char *Dest, unsigned char *XorFlags, unsigned char *XorBits)
{
// IMAGE TYPE 0x0A or 0x07                ; ED80h
//
// XOR-Repeat, Rows
//
// Format:
//  0x02                   Image type byte, byte that got us this far.
//   <Special Flag Byte>   Special 8-bit value that is used to signal repeats
//   <data starts here>
//
// Special XOR encoding.  This encoding scheme writes to the DMD in ROWS from
// the TOP to BOTTOM of the DMD starting at the top-left and ending at the
// bottom right of the display.
//
// Each byte is read from the data.  If a byte doesn't match the <Special Flag
// Byte> (first byte) then the byte is simply drawn to the DMD ram.  As with all
// encoding schemes the image for each of the 16 colums is actually drawn in
// reverse as it appears in ram.
//
// If the next data byte that is read DOES match the <Special Flag Byte> then
// the next 2 bytes are read, this makes a 3-byte pattern in the following
// manner:
//
//  <Special Flag Byte>  <Repeat Count>  <XOR Value>
//
// When the <Special Flag Byte> is encountered, then the next 2 bytes represent
// the <Repeat Count> and <XOR Value>.  The XOR Value is applied to the
// EXISTING DMD ram for the number of bytes defined in <Repeat Count>.  That is,
// the existing data in the RAM is XORed with the <XOR Value> for the number of
// bytes in <Repeat Count>.
//
	Decode_06or07(Source, &Dest, &XorFlags, &XorBits, WRITE_TYPE_ROWS);
}

void DMD::Decode_06or07(unsigned char **SourcePtr, unsigned char **DestPtr, unsigned char **XorFlagsPtr, unsigned char **XorBitsPtr, unsigned char Type)
{
	unsigned char ch;
	unsigned char SpecialFlagByte;
	unsigned int WriteCounter;
	unsigned int XorFlagsCounter;
	unsigned int XorBitsCounter;

	SpecialFlagByte = **SourcePtr;
	(*SourcePtr)++;
    if ((*SourcePtr) >= CommonData.EndPtr)
    {
       return;
    }
	WriteCounter = XorFlagsCounter = XorBitsCounter = 0; // Stores bytes we've written to DMD Ram
	do
	{
		ch = **SourcePtr;
		(*SourcePtr)++;
        if ((*SourcePtr) >= CommonData.EndPtr)
        {
           return;
        }
		if (ch == SpecialFlagByte)
		{
			unsigned char Value1 = **SourcePtr;
			(*SourcePtr)++;
            if ((*SourcePtr) >= CommonData.EndPtr)
            {
               return;
            }
			unsigned int Value2 = **SourcePtr;
			(*SourcePtr)++;
            if ((*SourcePtr) >= CommonData.EndPtr)
            {
               return;
            }
			do
			{
				WriteNext8BitValue(DestPtr,&WriteCounter, 0x00, Type);
				WriteNext8BitValue(XorFlagsPtr,&XorFlagsCounter, 0xFF, Type);
				WriteNext8BitValue(XorBitsPtr,&XorBitsCounter, Value2, Type);
			} while ((--Value1) && (WriteCounter < DMD_PAGE_BYTES));
		}
		else
		{
			WriteNext8BitValue(DestPtr,&WriteCounter, ch, Type);
			WriteNext8BitValue(XorFlagsPtr,&XorFlagsCounter,0x00,Type);
			WriteNext8BitValue(XorBitsPtr,&XorBitsCounter,0x00,Type);
		}
	} while (WriteCounter < DMD_PAGE_BYTES);
}

void DMD::Decode_08(unsigned char **Source, unsigned char *Dest, unsigned char *Skipped)
{
// IMAGE TYPE 0x0B or 0x08                ; EC91h
//
// Bulk Skips and Bulk Repeats, Columns
//
// Format:
//  Stream of Bytes:
//   <StartWithDataRepeatFlag>
//              |
//              |       Start Value is zero-->
//              +----------------------------------------\
//              |                                        |
//              |                                        |
//     <NonZeroRepeatPattern> [RepeatThePattern] --> <SkipCount> --> [PerformBulkSkip]
//              |                                                          |
//              |                                           <-- when done  |
//              \----------------------------------------------------------/
//
// This is identical to IMAGE TYPE 0x0C or 0x09 except data is drawn to DMD ram
// in COLUMNS left to right.
//
// This encoding scheme is a sequential reading of the data bytes and cycle of
// repeated data or row-per-column skipping.  This starts out reading the
// very first byte of the data and if it is zero, the loop starts at the right
// side of the diagram above at <SkipCount>.  If the first byte is non-zero then
// the loop starts at the left side of the diagram above at
// <NonZeroRepeatPattern>.
//
// When processing <NonZeroRepeatPattern>, if the byte is non-zero then the
// subsequent byte is read and repeated for the number of times defined in the
// previously read byte <NonZeroRepeatPattern>.  After doing this pattern
// repeat, the <SkipCount> byte is read.  The 8-bit rows-per-column are skipped
// for the number of times defined in <SkipCount>.  After skipping 8-bit rows
// in the column (or across multiple columns), the loop goes back to evaluate
// <NonZeroRepeatPattern> and this cycle continues until the entire DMD ram has
// been filled.  Note the <SkipCount> value can be zero, this will cause no
// skipping to occur and immediate wrap around to <NonZeroRepeatPattern>.
//
// As with all encoding schemes, the data appears on the DMD in reverse, for
// each column as it is stored in ram.  This is for each of the 16 columns.
//
//
// *** It appears the above write-up is incorrect, the left half does NOT
// *** repeat the pattern, rather it is the count of the number of data bytes
// *** to read from the source and then write to DMD ram, not repeat.
//
	Decode_08or09(Source, &Dest, &Skipped, WRITE_TYPE_COLUMNS);
}

void DMD::Decode_09(unsigned char **Source, unsigned char *Dest, unsigned char *Skipped)
{
// IMAGE TYPE 0x0C or 0x09                ; EBFEh
//
// Bulk Skips and Bulk Repeats, Rows
//
// Format:
//  Stream of Bytes:
//   <StartWithDataRepeatFlag>
//              |
//              |       Start Value is zero-->
//              +----------------------------------------\
//              |                                        |
//              |                                        |
//     <NonZeroRepeatPattern> [RepeatThePattern] --> <SkipCount> --> [PerformBulkSkip]
//              |                                                          |
//              |                                           <-- when done  |
//              \----------------------------------------------------------/
//
// This is identical to IMAGE TYPE 0x0B or 0x08 except data is drawn to DMD ram
// in ROWS top to bottom.
//
// This encoding scheme is a sequential reading of the data bytes and cycle of
// repeated data or 8-bit skipping.  This starts out reading the very first byte
// of the data and if it is zero, the loop starts at the right side of the
// diagram above at <SkipCount>.  If the first byte is non-zero then the loop
// starts at the left side of the diagram above at <NonZeroRepeatPattern>.
//
// When processing <NonZeroRepeatPattern>, if the byte is non-zero then the
// subsequent byte is read and repeated for the number of times defined in the
// previously read byte <NonZeroRepeatPattern>.  After doing this pattern
// repeat, the <SkipCount> byte is read.  Then 8-bits are skipped for the number
// of times defined in <SkipCount>.  After repeatably skipping 8-bits the loop
// goes back to evaluate <NonZeroRepeatPattern> and this cycle continues until
// the entire DMD ram has been filled.  Note the <SkipCount> value can be zero,
// this will cause no skipping to occur and immediate wrap around to
// <NonZeroRepeatPattern>.
//
// As with all encoding schemes, the data appears on the DMD in reverse, for
// each column as it is stored in ram.  This is for each of the 16 columns.
//
// *** It appears the above write-up is incorrect, the left half does NOT
// *** repeat the pattern, rather it is the count of the number of data bytes
// *** to read from the source and then write to DMD ram, not repeat.
//
	Decode_08or09(Source, &Dest, &Skipped, WRITE_TYPE_ROWS);
}

void DMD::Decode_08or09(unsigned char **SourcePtr, unsigned char **DestPtr, unsigned char **SkippedPtr, unsigned char Type)
{
	unsigned char count;
	unsigned char pattern;
	unsigned int WriteCounter;
	unsigned int SkippedCounter;

	count = **SourcePtr;
	(*SourcePtr)++;
    if ((*SourcePtr) >= CommonData.EndPtr)
    {
        return;
    }
	WriteCounter = SkippedCounter = 0;         // Stores bytes we've written to DMD Ram
	if (!count)
	{
		goto RepeatSkips;
	}
	while (1)
	{
		count = **SourcePtr;
		(*SourcePtr)++;
        if ((*SourcePtr) >= CommonData.EndPtr)
        {
           return;
        }
		if (count)
		{
			do
			{
				pattern = **SourcePtr;
				(*SourcePtr)++;
                if ((*SourcePtr) >= CommonData.EndPtr)
                {
                   return;
                }
				WriteNext8BitValue(DestPtr,&WriteCounter, pattern, Type);
				WriteNext8BitValue(SkippedPtr,&SkippedCounter, 0x00, Type);
			}
			while ((--count) && (WriteCounter < DMD_PAGE_BYTES));
		}
		if (WriteCounter >= DMD_PAGE_BYTES)
		{
			break;
		}
RepeatSkips:
		count = **SourcePtr;
		(*SourcePtr)++;
        if ((*SourcePtr) >= CommonData.EndPtr)
        {
           return;
        }
		if (count)
		{
			do
			{
				WriteNext8BitValue(DestPtr,&WriteCounter, 0x00, Type);
				WriteNext8BitValue(SkippedPtr,&SkippedCounter,0xFF, Type);
			}
			while ((--count) && (WriteCounter < DMD_PAGE_BYTES));
		}
		if (WriteCounter >= DMD_PAGE_BYTES)
		{
			break;
		}
	}
}

void DMD::Decode_0A(unsigned char **Source, unsigned char *Dest, unsigned char *Skipped)
{
// IMAGE TYPE 0x0D or 0x0A                ; EBFEh
//
// Write Data Bytes or Multiple Skips, Columns
//
// Format:
//  0x04                   Image type byte, byte that got us this far.
//   <Special Byte 1>      Special #1  Can be used for bitmap data.
//   <Special Byte 2>      Special #2  Can be used for bitmap data.
//   <Special Byte 3>      Special #3  Can be used for bitmap data.
//   <Special Byte 4>      Special #4  Can be used for bitmap data.
//   <Special Byte 5>      Special #5  Can be used for bitmap data.
//   <Special Byte 6>      Special #6  Can be used for bitmap data.
//   <Special Byte 7>      Special #7  Can be used for bitmap data.
//   <Special Byte 8>      Special #8  Can be used for bitmap data.
//    <data starts here>
//
//   Data Format (following the 8-byte header)
//   -----------------------------------------
//   <StartWithDataRepeatFlag>
//              |
//              |       Start Value is zero-->
//              +---------------------------------\
//              |                                 |
//              |                                 |
//        <DataLoadCount> [LoadDtaBytes] --> <SkipCount> --> [PerformBulkSkip]
//              |                                                    |
//              |                                     <-- when done  |
//              \----------------------------------------------------/
//
// This encoding scheme is identical to IMAGE TYPE 0x0E or 0x0B except this
// scheme writes the data on the DMD ram in COLUMNS.
//
// This encoding scheme first starts with the 8-byte header.  This is used by the
// F322 function call which will read the data as a continuous bit-stream
// starting at the 0x80 bit of the first byte and continuously working until the
// DMD ram has been filled.  The F322 function checks for the 1 extension bit
// to be set and if it is then the 8-byte header is used to index a particular
// 8-bit pattern that should be used.  If the index bit is zero, the F322
// function simply returns the 8-bits following the 0 non-extension bit.
//
// The data is written to the DMD ram in rows from LEFT to RIGHT.
//
// The diagram above shows the sequence of events, the very first data byte
// (after the 8-byte header) is used to determine of the cycle should begin
// at the right side <SkipCount> or the left side <DataLoadCount>.
//
// While processing through the loop, the <DataLoadCount> value indicates the
// number of 8-bit values that should be drawn to the DMD ram.  The number F322
// function is called for the number of times defined in <DataLoadCount>.  If
// this value is zero there is no bytes to load and the <SkipCount> is checked
// next.
//
// While processing through the loop, the <SkipCount> value indicates the number
// of 8-bit bytes that should be skipped in the DMD ram.  If this value is zero
// then there is no skipping and the following byte is read as the
// <DataLoadCount> value.
//
	Decode_0Aor0B(Source, &Dest, &Skipped, WRITE_TYPE_COLUMNS);
}

void DMD::Decode_0B(unsigned char **Source, unsigned char *Dest, unsigned char *Skipped)
{
// IMAGE TYPE 0x0E or 0x0B                ; EBC6h
//
// Write Data Bytes or Multiple Skips, Rows
//
// Format:
//  0x04                   Image type byte, byte that got us this far.
//   <Special Byte 1>      Special #1  Can be used for bitmap data.
//   <Special Byte 2>      Special #2  Can be used for bitmap data.
//   <Special Byte 3>      Special #3  Can be used for bitmap data.
//   <Special Byte 4>      Special #4  Can be used for bitmap data.
//   <Special Byte 5>      Special #5  Can be used for bitmap data.
//   <Special Byte 6>      Special #6  Can be used for bitmap data.
//   <Special Byte 7>      Special #7  Can be used for bitmap data.
//   <Special Byte 8>      Special #8  Can be used for bitmap data.
//    <data starts here>
//
//   Data Format (following the 8-byte header)
//   -----------------------------------------
//   <StartWithDataRepeatFlag>
//              |
//              |       Start Value is zero-->
//              +---------------------------------\
//              |                                 |
//              |                                 |
//        <DataLoadCount> [LoadDtaBytes] --> <SkipCount> --> [PerformBulkSkip]
//              |                                                    |
//              |                                     <-- when done  |
//              \----------------------------------------------------/
//
// This encoding scheme is identical to IMAGE TYPE 0x0D or 0x0A except this
// scheme writes the data on the DMD ram in ROWS.
//
// This encoding scheme first starts with the 8-byte header.  This is used by the
// F322 function call which will read the data as a continuous bit-stream
// starting at the 0x80 bit of the first byte and continuously working until the
// DMD ram has been filled.  The F322 function checks for the 1 extension bit
// to be set and if it is then the 8-byte header is used to index a particular
// 8-bit pattern that should be used.  If the index bit is zero, the F322
// function simply returns the 8-bits following the 0 non-extension bit.
//
// The data is written to the DMD ram in columns from TOP to BOTTOM.
//
// The diagram above shows the sequence of events, the very first data byte
// (after the 8-byte header) is used to determine of the cycle should begin
// at the right side <SkipCount> or the left side <DataLoadCount>.
//
// While processing through the loop, the <DataLoadCount> value indicates the
// number of 8-bit values that should be drawn to the DMD ram.  The number F322
// function is called for the number of times defined in <DataLoadCount>.  If
// this value is zero there is no bytes to load and the <SkipCount> is checked
// next.
//
// While processing through the loop, the <SkipCount> value indicates the number
// of 8-bit bytes that should be skipped in the DMD ram.  If this value is zero
// then there is no skipping and the following byte is read as the
// <DataLoadCount> value.
//
	Decode_0Aor0B(Source, &Dest, &Skipped, WRITE_TYPE_ROWS);
}

void DMD::Decode_0Aor0B(unsigned char **SourcePtr, unsigned char **DestPtr, unsigned char **SkippedPtr, unsigned char Type)
{
	ImageHeader Header;
	unsigned char count;
	int i;
	unsigned int WriteCounter;
	unsigned int SkippedCounter;

	Header.ReadMask = 0x80;
	WriteCounter = SkippedCounter = 0;         // Stores bytes we've written to DMD Ram

	for (i = 0; i < 8; i++)
	{
		Header.RepeatBytes[i] = **SourcePtr;
		(*SourcePtr)++;
        if ((*SourcePtr) >= CommonData.EndPtr)
        {
           return;
        }
	}
	count = ReadNext8BitValue(&Header,SourcePtr);
    if ((*SourcePtr) >= CommonData.EndPtr)
    {
       return;
    }
	if (!count)
	{
		goto BulkSkips;
	}
	while (1)
	{
		count = ReadNext8BitValue(&Header,SourcePtr);
        if ((*SourcePtr) >= CommonData.EndPtr)
        {
           return;
        }
		if (count)
		{
			do
			{
				WriteNext8BitValue(DestPtr,&WriteCounter, (ReadNext8BitValue(&Header,SourcePtr)), Type);
                if ((*SourcePtr) >= CommonData.EndPtr)
                {
                   return;
                }
				WriteNext8BitValue(SkippedPtr,&SkippedCounter, 0x00, Type);
			} while ((--count) && (WriteCounter < DMD_PAGE_BYTES));
		}
		if (WriteCounter >= DMD_PAGE_BYTES)
		{
			break;
		}
BulkSkips:
		count = ReadNext8BitValue(&Header,SourcePtr);
        if ((*SourcePtr) >= CommonData.EndPtr)
        {
           return;
        }
		if (count)
		{
			do
			{
				WriteNext8BitValue(DestPtr,&WriteCounter, 0x00, Type);
				WriteNext8BitValue(SkippedPtr,&SkippedCounter, 0xFF, Type);
			}
			while ((--count) && (WriteCounter < DMD_PAGE_BYTES));
		}
		if (WriteCounter >= DMD_PAGE_BYTES)
		{
			break;
		}
	} 
	if (Header.ReadMask == 0x80)
	{
		(*SourcePtr)--;
	}
}

void DMD::ButtonHandlerNext(int count)
{
#if ALLOW_MOUSE_TO_REPEAT
	int i = 0;
	if (NextDebounceState == DEBOUNCE_STATE_DONE)
	{
		i++;
	}
	NextDebounceState = DEBOUNCE_STATE_IDLE;
	NextDebounce = 0;
	if (i)
	{
		return;
	}
#endif

	CheckKeyStateForDebugFlags();

/*	if (!NaggedOnce)
	{
		if (!(PassedInPointer->MiscNagsShown[NAG_INDEX_DMD_ENTERKEY_TIP]))
		{
			unsigned char TheCheckBox = FALSE;
			NagDlg Nag(this, "Tip", (char *)&NagTexts[NAG_INDEX_DMD_ENTERKEY_TIP][0], &TheCheckBox);
			Nag.DoModal();
			if (TheCheckBox)
			{
				PassedInPointer->MiscNagsShown[NAG_INDEX_DMD_ENTERKEY_TIP] = TRUE;
				AfxGetApp()->WriteProfileInt(REGISTRY_NAG_SCREENS, NagRegistryKeyText[NAG_INDEX_DMD_ENTERKEY_TIP], TRUE);
			}
		}
	}*/
	NaggedOnce = 1;

	DecodeNextIndex(count);
}

void DMD::OnButtonNextGraphic() 
{
   ButtonHandlerNext(1);
}

void DMD::OnButtonNextGraphicx2() 
{
   ButtonHandlerNext(2);
}

void DMD::OnButtonNextGraphicAll() 
{
	int countInvalid = 0;
   unsigned long index = 0;
   while( countInvalid<200 ) {
	    DecodeFullFrameGraphic(index);
		if( FullFrameImageData.Planes.Plane0.Plane_Status !=  PLANE_STATUS_VALID ) countInvalid++;
		index += 2;	
   }
}

void DMD::ButtonHandlerPrevious(int count)
{
#if ALLOW_MOUSE_TO_REPEAT
	int i = 0;
	if (PreviousDebounceState == DEBOUNCE_STATE_DONE)
	{
		i++;
	}
	PreviousDebounceState = DEBOUNCE_STATE_IDLE;
	PreviousDebounce = 0;
	if (i)
	{
		return;
	}
#endif

	CheckKeyStateForDebugFlags();

	DecodePreviousIndex(count);
}

void DMD::OnButtonPreviousGraphic() 
{
   ButtonHandlerPrevious(1);
}

void DMD::OnButtonPreviousGraphicx2() 
{
   ButtonHandlerPrevious(2);
}

void DMD::InvalidateDMDPages()
{
	RECT ThisRect;
	GetClientRect(&ThisRect);
	//	
	ThisRect.bottom = ((DMD_ROWS + 1 + DMD_ROWS + 1 + DMD_ROWS) * PIXEL_HEIGHT);
	ThisRect.right = (DMD_COLUMNS * PIXEL_WIDTH);
	//	
	InvalidateRect(&ThisRect, FALSE);
}

void DMD::UpdateStaticTextBoxesFullFrameGraphics()
{
	CString str;

	if (FullFrameImageData.Planes.Plane0.Plane_Status > PLANE_STATUS_IMAGEOUTOFRANGE)
	{
		FullFrameImageData.Planes.Plane0.Plane_Status = PLANE_STATUS_IMAGEOUTOFRANGE;
	}
	if (FullFrameImageData.Planes.Plane1.Plane_Status > PLANE_STATUS_IMAGEOUTOFRANGE)
	{
		FullFrameImageData.Planes.Plane1.Plane_Status = PLANE_STATUS_IMAGEOUTOFRANGE;
	}

	str.Format("Index %1.1u\n\nROM Addr:\n0x%05x\n%1.1u Bytes\n\n%s",FullFrameImageData.CurrentImageIndex,(FullFrameImageData.TableAddress+(FullFrameImageData.CurrentImageIndex*3)),FullFrameImageData.Planes.Plane0.Plane_Size,StatusText[FullFrameImageData.Planes.Plane0.Plane_Status]);
	m_Dmd1.SetWindowText(str);
	str.Format("Index %1.1u\n\nROM Addr:\n0x%05x\n%1.1u Bytes\n\n%s",(FullFrameImageData.CurrentImageIndex + 1),(FullFrameImageData.TableAddress+((FullFrameImageData.CurrentImageIndex+1)*3)),FullFrameImageData.Planes.Plane1.Plane_Size,StatusText[FullFrameImageData.Planes.Plane1.Plane_Status]);
	m_Dmd2.SetWindowText(str);
	str.Format("Index %1.1u\n%s\n<and>\nIndex %1.1u\n%s",FullFrameImageData.CurrentImageIndex,StatusText[FullFrameImageData.Planes.Plane0.Plane_Status], (FullFrameImageData.CurrentImageIndex + 1),StatusText[FullFrameImageData.Planes.Plane1.Plane_Status]);
	m_Dmd3.SetWindowText(str);
}

void DMD::UpdateStaticTextBoxesVariableSizedImagePrint(int TableIndex, int ImageIndex, CStatic *pWnd, CStatic *pWndTitle, unsigned char Status)
{
	CString str;
	CString strTableType;
	CString strImageType;
	CString strAscii;
	CString strStatus;
	unsigned long TableAddr;
	unsigned long ImageAddr;

	switch (dialogType)
	{
		case DMD_DIALOG_TYPE_FONTDATA:
			strTableType = "Font";
			strImageType = "Char";
			strAscii.Format("ASCII: %c",((ImageIndex >= 0x20) && (ImageIndex < 0x7F))?ImageIndex:' ');
			break;

		case DMD_DIALOG_TYPE_ANIDATA:
			strTableType = "Animation";
			strImageType = "Frame";
			strAscii = "";
			break;

		default:
			strTableType = "Table";
			strImageType = "Index";
			strAscii = "";
			break;
	}

	str.Format("%s\n %d of %d",strTableType,TableIndex+1,VariableSizedImageData.maxTableIndex+1);
	pWndTitle->SetWindowText(str);

	//
	if (GetROMAddressOfVariableSizedImageTable(&TableAddr, TableIndex) != 0)
	{
		ImageAddr = 0;
	}
	if (GetROMAddressOfVariableSizedImageIndex(&ImageAddr, TableIndex, ImageIndex) != 0)
	{
		TableAddr = 0;
	}

	if (Status == PLANE_STATUS_VALID)
	{
		strStatus.Format("%d%s x %d%s",
			VariableSizedImageData.CurrentImageXSize,
			(VariableSizedImageData.CurrentImageXShift > 0)?"(+)":"",
			VariableSizedImageData.CurrentImageYSize,
			(VariableSizedImageData.CurrentImageYShift > 0)?"(+)":"");
	}
	else
	{
		strStatus = "**ERROR**";
	}

	str.Format("%s 0x%02x\n%s\nROM Addrs:\nTable:\n0x%05x\n%s:\n0x%05x\n%s",strImageType,ImageIndex,strAscii,TableAddr,strImageType,ImageAddr,strStatus);
	pWnd->SetWindowText(str);
}

void DMD::UpdateStaticTextBoxesVariableSizedImagePane(int Pane)
{
	CString str;

	switch (Pane)
	{
		case 1:
			UpdateStaticTextBoxesVariableSizedImagePrint(VariableSizedImageData.CurrentTableIndex,VariableSizedImageData.CurrentImageIndex,&m_Dmd1,&m_Dmd1Title,VariableSizedImageData.Planes.Plane0.Plane_Status);
			break;
		case 2:
			if (VariableSizedImageData.Planes.Plane1.Plane_Status == PLANE_STATUS_VALID)
			{
				UpdateStaticTextBoxesVariableSizedImagePrint(VariableSizedImageData.CurrentTableIndex,VariableSizedImageData.CurrentImageIndex,&m_Dmd2,&m_Dmd2Title,VariableSizedImageData.Planes.Plane1.Plane_Status);
			}
			else
			{
				m_Dmd2Title.SetWindowText("");
				m_Dmd2.SetWindowText("");
			}
			break;
		case 3:
			if (VariableSizedImageData.Planes.Plane1.Plane_Status == PLANE_STATUS_VALID)
			{
				UpdateStaticTextBoxesVariableSizedImagePrint(VariableSizedImageData.CurrentTableIndex,VariableSizedImageData.CurrentImageIndex,&m_Dmd3,&m_Dmd3Title,
					((VariableSizedImageData.Planes.Plane0.Plane_Status == PLANE_STATUS_VALID)&&(VariableSizedImageData.Planes.Plane1.Plane_Status == PLANE_STATUS_VALID))?PLANE_STATUS_VALID:PLANE_STATUS_INVALID);;
			}
			else
			{
				m_Dmd3Title.SetWindowText("");
				m_Dmd3.SetWindowText("");
			}
			break;
		default:
			break;
	}
}

void DMD::UpdateStaticTextBoxesVariableSizedImage()
{
	UpdateStaticTextBoxesVariableSizedImagePane(1);
	UpdateStaticTextBoxesVariableSizedImagePane(2);
	UpdateStaticTextBoxesVariableSizedImagePane(3);
}

void DMD::UpdateStaticTextBoxes()
{
	switch (dialogType)
	{
		case DMD_DIALOG_TYPE_GRAPHICS:
			UpdateStaticTextBoxesFullFrameGraphics();
			break;

		case DMD_DIALOG_TYPE_FONTDATA:
		case DMD_DIALOG_TYPE_ANIDATA:
			UpdateStaticTextBoxesVariableSizedImage();
			break;

		default:
			break;
	}
}

void DMD::UpdateControls()
{
	BOOL bEnablePrev = FALSE;
	BOOL bEnablePrevX2 = FALSE;
	BOOL bEnableNext = FALSE;
	BOOL bEnableNextX2 = FALSE;

	switch (dialogType)
	{
		case DMD_DIALOG_TYPE_GRAPHICS:
			if (FullFrameImageData.CurrentImageIndex > 0)
			{
				bEnablePrev = TRUE;
			}
            if (FullFrameImageData.CurrentImageIndex > 1)
            {
                bEnablePrevX2 = TRUE;
            }
			//if (FullFrameImageData.CurrentImageIndex < MAX_GRAPHIC_INDEX)
			{
				bEnableNext = TRUE;
                bEnableNextX2= TRUE;
			}
			break;

		case DMD_DIALOG_TYPE_FONTDATA:
		case DMD_DIALOG_TYPE_ANIDATA:
			if ((VariableSizedImageData.CurrentTableIndex > VariableSizedImageData.minTableIndex) || ((VariableSizedImageData.CurrentTableIndex == VariableSizedImageData.minTableIndex) && (VariableSizedImageData.CurrentImageIndex > VariableSizedImageData.minImageIndex)))
			{
				bEnablePrev = TRUE;
			}
			if ((VariableSizedImageData.CurrentTableIndex > VariableSizedImageData.minTableIndex) || ((VariableSizedImageData.CurrentTableIndex == VariableSizedImageData.minTableIndex) && (VariableSizedImageData.CurrentImageIndex > VariableSizedImageData.minImageIndex+1)))
			{
				bEnablePrevX2 = TRUE;
			}
			if ((VariableSizedImageData.CurrentTableIndex < VariableSizedImageData.maxTableIndex) || ((VariableSizedImageData.CurrentTableIndex == VariableSizedImageData.maxTableIndex) && (VariableSizedImageData.CurrentImageIndex < VariableSizedImageData.maxImageIndex)))
			{
				bEnableNext = TRUE;
			}
			if ((VariableSizedImageData.CurrentTableIndex < VariableSizedImageData.maxTableIndex) || ((VariableSizedImageData.CurrentTableIndex == VariableSizedImageData.maxTableIndex) && (VariableSizedImageData.CurrentImageIndex < VariableSizedImageData.maxImageIndex-1)))
			{
				bEnableNextX2 = TRUE;
			}
			break;

		default:
			break;
	}

	//
	m_PreviousGraphic.EnableWindow(bEnablePrev);
	m_NextGraphic.EnableWindow(bEnableNext);
	m_PreviousGraphicX2.EnableWindow(bEnablePrevX2);
	m_NextGraphicX2.EnableWindow(bEnableNextX2);
}

void DMD::OnCheckSkipped() 
{
	InvalidateDMDPages();
}

void DMD::OnCheckExport() {
	actTime = time(NULL);
}

void DMD::OnCheckXored() 
{
	InvalidateDMDPages();
}


void DMD::OnSelchangeList1() 
{
	InvalidateDMDPages();
}

void DMD::OnOK() 
{
	SaveDMDRegistrySettings();	
	CDialog::OnOK();
}

void DMD::OnClose() 
{
	SaveDMDRegistrySettings();	
	CDialog::OnClose();
}

void DMD::SaveDMDRegistrySettings()
{
	PassedInPointer->PixelColor = m_PixelColor.GetTopIndex();
	PassedInPointer->XoredCheckboxState = m_Xored.GetCheck();
	PassedInPointer->SkippedCheckboxState = m_Skipped.GetCheck();
	((CHexEditorApp *)AfxGetApp())->SaveProgramSettingsToRegistry(PassedInPointer);
}

void DMD::UpdateCheckboxText()
{
	CString CurrentText;
	CString DesiredText;
	int CurrentColor = m_PixelColor.GetTopIndex();
	int TextStringColor;
	TextStringColor = NORMAL_XORED_COLOR;
	if (CurrentColor == NORMAL_XORED_COLOR)
	{
		TextStringColor = ALTERNATE_XORED_COLOR;
	}
	DesiredText.Format("Show XORed pixels as %s",ColorText[TextStringColor]);
	m_Xored.GetWindowText(CurrentText);
	if (CurrentText != DesiredText)
	{
		m_Xored.SetWindowText(DesiredText);
	}

	TextStringColor = NORMAL_SKIPPED_COLOR;
	if (CurrentColor == NORMAL_SKIPPED_COLOR)
	{
		TextStringColor = ALTERNATE_SKIPPED_COLOR;
	}
	DesiredText.Format("Show Skipped pixels as %s",ColorText[TextStringColor]);
	m_Skipped.GetWindowText(CurrentText);
	if (CurrentText != DesiredText)
	{
		m_Skipped.SetWindowText(DesiredText);
	}
}

HBRUSH DMD::OnCtlColor(CDC* pDC, CWnd* pWnd, UINT nCtlColor) 
{
	HBRUSH hbr = CDialog::OnCtlColor(pDC, pWnd, nCtlColor);

//#define CTLCOLOR_MSGBOX         0
//#define CTLCOLOR_EDIT           1
//#define CTLCOLOR_LISTBOX        2
//#define CTLCOLOR_BTN            3
//#define CTLCOLOR_DLG            4
//#define CTLCOLOR_SCROLLBAR      5
//#define CTLCOLOR_STATIC         6
//#define CTLCOLOR_MAX            7
//	if (nCtlColor == CTLCOLOR_DLG)
//	{
//		pDC->SetTextColor(GetSysColor(COLOR_INACTIVECAPTION));
//		pDC->SetBkColor(RGB(0,0,0));
//		return (HBRUSH)(m_pListBkBrush->GetSafeHandle());
//	}
	return hbr;
}

void DMD::OnShowWindow(BOOL bShow, UINT nStatus) 
{
	CDialog::OnShowWindow(bShow, nStatus);
	UpdateControls();
	GotoDlgCtrl (GetDlgItem(IDC_BUTTON_NEXT_GRAPHIC));
}

void DMD::OnTimer(UINT nIDEvent) 
{
#if ALLOW_MOUSE_TO_REPEAT
#define CLEAR_NEXT      0x01
#define CLEAR_PREVIOUS  0x02

	unsigned char Clear = (CLEAR_NEXT | CLEAR_PREVIOUS);

	if (nIDEvent == TIMER_DMD)
	{
		if (IsWindowVisible())
		{
			CPoint pos;
			CRect rec;
			BOOL LeftButtonDown = FALSE;
			if (GetSystemMetrics(SM_SWAPBUTTON))
			{
				if ((GetAsyncKeyState(VK_RBUTTON)) < 0)
					LeftButtonDown = TRUE;
			}
			else
			{
				if ((GetAsyncKeyState(VK_LBUTTON)) < 0)
					LeftButtonDown = TRUE;
			}
			if (LeftButtonDown == TRUE)
			{
				if (GetCursorPos(&pos))
				{
					m_NextGraphic.GetWindowRect(&rec);
					if (rec.PtInRect(pos)) 
					{
						Clear &= ~CLEAR_NEXT;
						switch (NextDebounceState)
						{
							case DEBOUNCE_STATE_DONE        :
								DecodeNextIndex(1);
								break;
							case DEBOUNCE_STATE_DEBOUNCING  :
								if (NextDebounce)
									NextDebounce--;
								if (!NextDebounce)
									NextDebounceState = DEBOUNCE_STATE_DONE;
								break;
							case DEBOUNCE_STATE_IDLE        :
							default :
								NextDebounce = (DEFAULT_DEBOUNCE_TIME / TIMER_DMD_UPDATE);
								NextDebounceState = DEBOUNCE_STATE_DEBOUNCING;
						}
					}
					else
					{
						m_PreviousGraphic.GetWindowRect(&rec);
						if ((rec.PtInRect(pos)) && (m_PreviousGraphic.GetFocus()))
						{
							Clear &= ~CLEAR_PREVIOUS;
							switch (PreviousDebounceState)
							{
								case DEBOUNCE_STATE_DONE        :
									DecodePreviousIndex(1);
									break;
								case DEBOUNCE_STATE_DEBOUNCING  :
									if (PreviousDebounce)
										PreviousDebounce--;
									if (!PreviousDebounce)
										PreviousDebounceState = DEBOUNCE_STATE_DONE;
									break;
								case DEBOUNCE_STATE_IDLE        :
								default :
									PreviousDebounce = (DEFAULT_DEBOUNCE_TIME / TIMER_DMD_UPDATE);
									PreviousDebounceState = DEBOUNCE_STATE_DEBOUNCING;
							}
						}
					}
				}
			}
		}
	}	
	if (Clear & CLEAR_NEXT)
	{
		NextDebounce = 0;
		NextDebounceState = DEBOUNCE_STATE_IDLE;
	}
	if (Clear & CLEAR_PREVIOUS)
	{
		PreviousDebounce = 0;
		PreviousDebounceState = DEBOUNCE_STATE_IDLE;
	}
	CDialog::OnTimer(nIDEvent);
#endif
}

void DMD::OnLButtonDown(UINT nFlags, CPoint point) 
{
	CPoint pos;
	CRect rec;
	int InButton = 0;
    int InTitleBox = 0;
    CStatic *pTitleBox = NULL;

	if (GetCursorPos(&pos))
	{
		m_NextGraphic.GetWindowRect(&rec);
		if (rec.PtInRect(pos))
		{
			InButton = 1;
		}
		m_NextGraphicX2.GetWindowRect(&rec);
		if (rec.PtInRect(pos))
		{
			InButton = 1;
		}
		m_PreviousGraphic.GetWindowRect(&rec);
		if (rec.PtInRect(pos))
		{
			InButton = 1;
		}
		m_PreviousGraphicX2.GetWindowRect(&rec);
		if (rec.PtInRect(pos))
		{
			InButton = 1;
		}
        m_Dmd1Title.GetWindowRect(&rec);
        if (rec.PtInRect(pos))
        {
            InTitleBox = 1;
            pTitleBox = &m_Dmd1Title;
        }
        m_Dmd2Title.GetWindowRect(&rec);
        if (rec.PtInRect(pos))
        {
            InTitleBox = 2;
            pTitleBox = &m_Dmd2Title;
        }
        m_Dmd3Title.GetWindowRect(&rec);
        if (rec.PtInRect(pos))
        {
            InTitleBox = 3;
            pTitleBox = &m_Dmd3Title;
        }
	}
	if (!InButton && !InTitleBox)
	{
		PostMessage(WM_NCLBUTTONDOWN, HTCAPTION, MAKELPARAM(point.x, point.y));
	}
    if (InTitleBox && (pTitleBox != NULL))
    {
        CString str;
        pTitleBox->GetWindowText(str);
        if (InTitleBox == selectedTitleBox)
        {
           // They re-clicked the currently selected title box, so unselect it
           pTitleBox->SetWindowText("Clipboard Off");
           selectedTitleBox = 0;
        }
        else
        {
           // They clicked a new title box, set it as the currently selected title box
           pTitleBox->SetWindowText("Clipboard On");
           selectedTitleBox = InTitleBox;
           OnPaint();  // get current clipboard pane data
        }
        Sleep(500);
        pTitleBox->SetWindowText(str);
    }
	CDialog::OnLButtonDown(nFlags, point);
}

void DMD::OnLButtonUp(UINT nFlags, CPoint point) 
{
	CDialog::OnLButtonUp(nFlags, point);
}


void DMD::OnButtonWipe() 
{
	memset(PreviousPlaneDataPane0,0,sizeof(PreviousPlaneDataPane0));
	memset(PreviousPlaneDataPane1,0,sizeof(PreviousPlaneDataPane1));

	m_Wipe.EnableWindow(FALSE);
    bWiped = TRUE;

	InvalidateDMDPages();
}
```
