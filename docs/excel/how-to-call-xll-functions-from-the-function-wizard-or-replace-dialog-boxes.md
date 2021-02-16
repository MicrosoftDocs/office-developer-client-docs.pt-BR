---
title: Chamar funções XLL do Assistente de Função ou substituir caixas de diálogo
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
keywords:
- funções xll [excel 2007], chamando de substituir caixa de diálogo, substituir caixa de diálogo [Excel 2007], chamando funções XLL,Assistente de Função [Excel 2007], chamando funções XLL,funções XLL [Excel 2007], chamando do Assistente de Função
localization_priority: Normal
ms.assetid: dc7e840e-6d1d-427b-97f9-7912e60ec954
description: 'Aplica-se a: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: 11189beed13e2ceb99ef04b7a2f966cb4171915c
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33410746"
---
# <a name="call-xll-functions-from-the-function-wizard-or-replace-dialog-boxes"></a><span data-ttu-id="35d99-104">Chamar funções XLL do Assistente de Função ou substituir caixas de diálogo</span><span class="sxs-lookup"><span data-stu-id="35d99-104">Call XLL Functions from the Function Wizard or Replace Dialog Boxes</span></span>

 <span data-ttu-id="35d99-105">**Aplica-se a**: Excel 2013 | Office 2013 | Visual Studio</span><span class="sxs-lookup"><span data-stu-id="35d99-105">**Applies to**: Excel 2013 | Office 2013 | Visual Studio</span></span> 
  
<span data-ttu-id="35d99-106">O Microsoft Excel geralmente chama funções XLL durante o recálculo normal da planilha ou uma parte dela se o cálculo estiver sob o controle de uma macro.</span><span class="sxs-lookup"><span data-stu-id="35d99-106">Microsoft Excel usually calls XLL functions during the normal recalculation of the workbook, or a part of it if the calculation is under the control of a macro.</span></span> <span data-ttu-id="35d99-107">Lembre-se de que a função pode não residir em uma fórmula de célula, mas pode fazer parte de uma definição de intervalo nomeada ou uma expressão de formatação condicional.</span><span class="sxs-lookup"><span data-stu-id="35d99-107">Remember that the function might not reside in a cell formula but might be part of a named range definition, or a conditional formatting expression.</span></span>
  
<span data-ttu-id="35d99-108">Há duas circunstâncias em que uma função pode ser chamada de uma caixa de diálogo do Excel.</span><span class="sxs-lookup"><span data-stu-id="35d99-108">There are two circumstances where a function can be called from an Excel dialog box.</span></span> <span data-ttu-id="35d99-109">Uma delas é a **caixa de diálogo Argumentos** da Função Colar, onde os usuários são capazes de construir uma chamada de função de um argumento por vez.</span><span class="sxs-lookup"><span data-stu-id="35d99-109">One is the **Paste Function Arguments** dialog box, where users are able to construct a function call one argument at a time.</span></span> <span data-ttu-id="35d99-110">A outra é quando as fórmulas estão sendo modificadas e reinserida pelo Excel na caixa **de** diálogo Substituir.</span><span class="sxs-lookup"><span data-stu-id="35d99-110">The other is when formulas are being modified and reentered by Excel in the **Replace** dialog box.</span></span> <span data-ttu-id="35d99-111">Para a **caixa de diálogo Argumentos da Função Colar,** talvez você não queira que sua função seja executada normalmente.</span><span class="sxs-lookup"><span data-stu-id="35d99-111">For the **Paste Function Arguments** dialog box, you might not want your function to execute normally.</span></span> <span data-ttu-id="35d99-112">Isso pode ser porque leva muito tempo para ser executado e você não deseja retardar o uso da caixa de diálogo.</span><span class="sxs-lookup"><span data-stu-id="35d99-112">This may be because it takes a long time to execute and you do not want to slow down the use of the dialog box.</span></span> 
  
<span data-ttu-id="35d99-113">Tanto a caixa de diálogo  **Colar Função** quanto a caixa de diálogo Substituir têm o nome de classe do Windows **bosa_sdm_XL** n, onde n é um número.</span><span class="sxs-lookup"><span data-stu-id="35d99-113">Both the **Paste Function** dialog box and the **Replace** dialog box have the Windows class name **bosa_sdm_XL** n, where n is a number.</span></span> <span data-ttu-id="35d99-114">O Windows fornece uma função de API, **GetClassName**, que obtém esse nome de um identificador do Windows, um tipo de variável HWND.</span><span class="sxs-lookup"><span data-stu-id="35d99-114">Windows provides an API function, **GetClassName**, that obtains this name from a Windows handle, an HWND variable type.</span></span> <span data-ttu-id="35d99-115">Ele também fornece outra função, **EnumWindows**, que chama uma função de retorno de chamada fornecida (dentro de sua DLL) uma vez para cada janela de nível superior que está aberta no momento.</span><span class="sxs-lookup"><span data-stu-id="35d99-115">It also provides another function, **EnumWindows**, that calls a supplied callback function (within your DLL) once for every top-level window that is currently open.</span></span>
  
<span data-ttu-id="35d99-116">A função de retorno de chamada precisa executar apenas as seguintes etapas:</span><span class="sxs-lookup"><span data-stu-id="35d99-116">The callback function needs to perform only the following steps:</span></span>
  
1. <span data-ttu-id="35d99-117">Verifique se o pai dessa janela é a instância atual do Excel (caso haja várias instâncias em execução).</span><span class="sxs-lookup"><span data-stu-id="35d99-117">Check if the parent of this window is the current instance of Excel (in case there are multiple instances running).</span></span>
    
2. <span data-ttu-id="35d99-118">Obter o nome da classe do alça passado pelo Windows.</span><span class="sxs-lookup"><span data-stu-id="35d99-118">Get the class name from the handle passed in by Windows.</span></span>
    
3. <span data-ttu-id="35d99-119">Verifique se o nome da classe tem o formato **bosa_sdm_XL** n.</span><span class="sxs-lookup"><span data-stu-id="35d99-119">Check if the class name is of the form **bosa_sdm_XL** n.</span></span>
    
4. <span data-ttu-id="35d99-120">Se você precisar distinguir entre as duas caixas de diálogo, verifique se o título da caixa de diálogo contém algum texto de identificação.</span><span class="sxs-lookup"><span data-stu-id="35d99-120">If you need to distinguish between the two dialog boxes, check if the dialog box title contains some identifying text.</span></span> <span data-ttu-id="35d99-121">O título da janela é obtido usando a chamada da API do Windows **GetWindowText**.</span><span class="sxs-lookup"><span data-stu-id="35d99-121">The window title is obtained using the Windows API call **GetWindowText**.</span></span>
    
<span data-ttu-id="35d99-122">O código C++ a seguir mostra uma classe e retorno de chamada a serem passados para o Windows que executa essas etapas.</span><span class="sxs-lookup"><span data-stu-id="35d99-122">The following C++ code shows a class and callback to be passed to Windows that performs these steps.</span></span> <span data-ttu-id="35d99-123">Isso é chamado pelas funções que chamam o teste especificamente para qualquer uma das caixas de diálogo em questão.</span><span class="sxs-lookup"><span data-stu-id="35d99-123">This is called by the functions that call test specifically for either of the dialog boxes concerned.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="35d99-124">Títulos de janela de versões futuras do Excel podem mudar e invalidar esse código.</span><span class="sxs-lookup"><span data-stu-id="35d99-124">Window titles of future Excel versions might change and invalidate this code.</span></span> <span data-ttu-id="35d99-125">Observe também que a **window_title_text** como **NULL** tem o efeito de ignorar o título da janela na pesquisa de retorno de chamada.</span><span class="sxs-lookup"><span data-stu-id="35d99-125">Note also that setting **window_title_text** to **NULL** has the effect of ignoring window title in the callback search.</span></span> 
  
```cs
#define CLASS_NAME_BUFFSIZE  50
#define WINDOW_TEXT_BUFFSIZE  50
// Data structure used as input to xldlg_enum_proc(), called by
// called_from_paste_fn_dlg(), called_from_replace_dlg(), and
// called_from_Excel_dlg(). These functions tell the caller whether
// the current worksheet function was called from one or either of
// these dialog boxes.
typedef struct
{
  bool is_dlg;
  short low_hwnd;
  char *window_title_text; // set to NULL if don't care
}
  xldlg_enum_struct;
// The callback function called by Windows for every top-level window.
BOOL CALLBACK xldlg_enum_proc(HWND hwnd, xldlg_enum_struct *p_enum)
{
// Check if the parent window is Excel.
// Note: Because of the change from MDI (Excel 2010)
// to SDI (Excel 2013), comment out this step in Excel 2013.
  if(LOWORD((DWORD)GetParent(hwnd)) != p_enum->low_hwnd)
    return TRUE; // keep iterating
  char class_name[CLASS_NAME_BUFFSIZE + 1];
//  Ensure that class_name is always null terminated for safety.
  class_name[CLASS_NAME_BUFFSIZE] = 0;
  GetClassName(hwnd, class_name, CLASS_NAME_BUFFSIZE);
//  Do a case-insensitve comparison for the Excel dialog window
//  class name with the Excel version number truncated.
  size_t len; // The length of the window's title text
  if(_strnicmp(class_name, "bosa_sdm_xl", 11) == 0)
  {
// Check if a searching for a specific title string
    if(p_enum->window_title_text) 
    {
// Get the window's title and see if it matches the given text.
      char buffer[WINDOW_TEXT_BUFFSIZE + 1];
      buffer[WINDOW_TEXT_BUFFSIZE] = 0;
      len = GetWindowText(hwnd, buffer, WINDOW_TEXT_BUFFSIZE);
      if(len == 0) // No title
      {
        if(p_enum->window_title_text[0] != 0)
          return TRUE; // No match, so keep iterating
      }
// Window has a title so do a case-insensitive comparison of the
// title and the search text, if provided.
      else if(p_enum->window_title_text[0] != 0
      && _stricmp(buffer, p_enum->window_title_text) != 0)
        return TRUE; // Keep iterating
    }
    p_enum->is_dlg = true;
    return FALSE; // Tells Windows to stop iterating.
  }
  return TRUE; // Tells Windows to continue iterating.
}
```

<span data-ttu-id="35d99-126">A caixa de diálogo Colar **Função** não tem um título, portanto, a função a seguir passa uma cadeia de caracteres de título de pesquisa de "", ou seja, uma cadeia de caracteres vazia, para o retorno de chamada para indicar que a condição de match é que a janela não deve ter um título.</span><span class="sxs-lookup"><span data-stu-id="35d99-126">The **Paste Function** dialog box does not have a title, so the following function passes a search title string of "", that is, an empty string, to the callback to indicate that the match condition is that the window should not have a title.</span></span> 
  
```cs
bool called_from_paste_fn_dlg(void)
{
    XLOPER xHwnd;
// Calls Excel4, which only returns the low part of the Excel
// main window handle. This is OK for the search however.
    if(Excel4(xlGetHwnd, &xHwnd, 0))
        return false; // Couldn't get it, so assume not
// Search for bosa_sdm_xl* dialog box with no title string.
    xldlg_enum_struct es = {FALSE, xHwnd.val.w, ""};
    EnumWindows((WNDENUMPROC)xldlg_enum_proc, (LPARAM)&es);
    return es.is_dlg;
}
```

## <a name="see-also"></a><span data-ttu-id="35d99-127">Confira também</span><span class="sxs-lookup"><span data-stu-id="35d99-127">See also</span></span>



[<span data-ttu-id="35d99-128">Acessar o código de XLL no Excel</span><span class="sxs-lookup"><span data-stu-id="35d99-128">Accessing XLL Code in Excel</span></span>](accessing-xll-code-in-excel.md)
  
[<span data-ttu-id="35d99-129">Calling into Excel from the DLL or XLL</span><span class="sxs-lookup"><span data-stu-id="35d99-129">Calling into Excel from the DLL or XLL</span></span>](calling-into-excel-from-the-dll-or-xll.md)
  
[<span data-ttu-id="35d99-130">Desenvolvimento de XLLs do Excel</span><span class="sxs-lookup"><span data-stu-id="35d99-130">Developing Excel XLLs</span></span>](developing-excel-xlls.md)

