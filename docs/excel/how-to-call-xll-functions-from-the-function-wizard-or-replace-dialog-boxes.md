---
title: Chamar funções de XLL no Assistente de função ou nas caixas de diálogo Substituir
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
keywords:
- funções de XLL [excel 2007], chamada a partir de caixa de diálogo Substituir, substituir diálogo caixa chamando funções XLL [Excel 2007], o Assistente de função [Excel 2007], chamar funções XLL, as funções XLL [Excel 2007], chamando do Assistente de função
localization_priority: Normal
ms.assetid: dc7e840e-6d1d-427b-97f9-7912e60ec954
description: 'Aplica-se a: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: 7ebb33a5b98cebedfca7fb5923e62486bfd85696
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19765386"
---
# <a name="call-xll-functions-from-the-function-wizard-or-replace-dialog-boxes"></a>Chamar funções de XLL no Assistente de função ou nas caixas de diálogo Substituir

 **Aplica-se a**: Excel 2013 | Office 2013 | Visual Studio 
  
Microsoft Excel geralmente chama funções XLL durante o recálculo normal da pasta de trabalho ou parte dela, se o cálculo está sob o controle de uma macro. Lembre-se de que a função não poderá residir em uma fórmula de célula, mas pode ser parte de uma definição de intervalo nomeado ou uma expressão de formatação condicional.
  
Existem duas circunstâncias onde uma função pode ser chamada a partir de uma caixa de diálogo do Excel. Uma é a caixa de diálogo **Argumentos da função colar** , onde os usuários são capazes de construir um argumento de uma chamada de função por vez. O outro é quando as fórmulas estão sendo modificado e restabelecida pelo Excel na caixa de diálogo **Substituir** . Para a caixa de diálogo **Argumentos da função colar** , talvez você não queira sua função para executar normalmente. Isso pode ser porque ele leva muito tempo para executar e você não deseja diminuir o uso da caixa de diálogo. 
  
A caixa de diálogo **Colar função** e a caixa de diálogo **Substituir** tem o Windows classe nome **bosa_sdm_XL**n, onde n é um número. O Windows fornece uma função de API, **GetClassName**, que obtém esse nome a partir de um manipulador de Windows, um tipo de variável HWND. Ele também oferece outra função, **EnumWindows**, que chama uma função de chamada de retorno fornecido (dentro da sua DLL) uma vez para cada janela de nível superior que está aberta no momento.
  
A função de retorno de chamada precisa executar somente as seguintes etapas:
  
1. Verifique se o pai dessa janela é a instância atual do Excel (caso haja várias instâncias em execução).
    
2. Obtenha o nome da classe da alça passada pelo Windows.
    
3. Verifique se o nome de classe é de n de **bosa_sdm_XL**o formulário.
    
4. Se você precisar distinguir entre duas caixas de diálogo, verifique se o título da caixa de diálogo contém alguns texto de identificação. O título da janela é obtido usando a chamada de API do Windows **GetWindowText**.
    
O código de C++ a seguir mostra uma classe e o retorno de chamada a serem passados para Windows que está executando estas etapas. Isso é chamado pelas funções do teste chamada especificamente para qualquer uma das caixas de diálogo em questão. 
  
> [!NOTE]
> Títulos de janela de futuras versões do Excel podem alterar e invalidar este código. Observe também que a definição de **window_title_text** como **Nulo** tem o efeito de ignorando o título da janela na pesquisa de retorno de chamada. 
  
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

A caixa de diálogo **Colar função** não possui um título, portanto a função a seguir passa uma cadeia de caracteres do título de pesquisa de "", ou seja, uma cadeia de caracteres vazia para o retorno de chamada para indicar que a condição de correspondência é que a janela não deve ter um título. 
  
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

## <a name="see-also"></a>Confira também



[Acessar o código de XLL no Excel](accessing-xll-code-in-excel.md)
  
[Calling into Excel from the DLL or XLL](calling-into-excel-from-the-dll-or-xll.md)
  
[Desenvolvimento de XLLs do Excel](developing-excel-xlls.md)

