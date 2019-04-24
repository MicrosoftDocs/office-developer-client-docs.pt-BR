---
title: IMAPIFormMgrSelectForm
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIFormMgr.SelectForm
api_type:
- COM
ms.assetid: c1cfe71b-01f3-429a-8b4c-73191a2ffea0
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: c25f352e7fa607a46741164574a4ba91d4026edf
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32321669"
---
# <a name="imapiformmgrselectform"></a>IMAPIFormMgr::SelectForm

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Apresenta uma caixa de diálogo que permite ao usuário selecionar um formulário e retorna um objeto de informações de formulário que descreve esse formulário.
  
```cpp
HRESULT SelectForm(
  ULONG_PTR ulUIParam,
  ULONG ulFlags,
  LPCSTR pszTitle,
  LPMAPIFOLDER pfld,
  LPMAPIFORMINFO FAR * ppfrminfoReturned
);
```

## <a name="parameters"></a>Parâmetros

 _ulUIParam_
  
> no Uma alça para a janela pai da caixa de diálogo exibida. 
    
 _ulFlags_
  
> no Uma máscara de bits de sinalizadores que controla o tipo das cadeias de caracteres passadas. O seguinte sinalizador pode ser definido:
    
MAPI_UNICODE 
  
> As cadeias de caracteres passadas estão no formato Unicode. Se o sinalizador MAPI_UNICODE não estiver definido, as cadeias de caracteres estarão no formato ANSI.
    
 _pszTitle_
  
> no Um ponteiro para uma cadeia de caracteres que contém a legenda da caixa de diálogo. Se o parâmetro _pszTitle_ for NULL, o provedor de biblioteca de formulários fornecerá uma legenda padrão. 
    
 _pfld_
  
> no Um ponteiro para a pasta na qual o formulário será selecionado. Se o parâmetro _pfld_ for NULL, o formulário pode ser selecionado do contêiner de formulários local, pessoal ou organização. 
    
 _ppfrminfoReturned_
  
> bota Um ponteiro para um ponteiro para o objeto de informações do formulário retornado.
    
## <a name="return-value"></a>Valor de retorno

S_OK 
  
> A chamada teve êxito e retornou o valor ou valores esperados.
    
MAPI_E_BAD_CHARWIDTH 
  
> O sinalizador MAPI_UNICODE foi definido e a implementação não tem suporte para Unicode ou o MAPI_UNICODE não foi definido e a implementação oferece suporte somente a Unicode.
    
MAPI_E_USER_CANCEL 
  
> O usuário cancelou a operação, geralmente clicando no botão **Cancelar** na caixa de diálogo. 
    
## <a name="remarks"></a>Comentários

Os visualizadores de formulários chamam o método **IMAPIFormMgr:: SelectForm** para primeiro apresentar uma caixa de diálogo que permite ao usuário selecionar um formulário e, em seguida, recuperar um objeto de informações de formulário que descreve o formulário selecionado. A caixa de diálogo restringe o usuário a selecionar um único Formulário. 
  
## <a name="notes-to-callers"></a>Notas para chamadores

A caixa de diálogo **SelectForm** exibe somente formulários que não estão ocultos (ou seja, formulários que têm suas propriedades ocultas desmarcadas). Se um visualizador de formulários passar o sinalizador MAPI_UNICODE no parâmetro _parâmetroulflags_ , todas as cadeias de caracteres serão Unicode. Os provedores de biblioteca de formulários que não dão suporte a cadeias de caracteres Unicode devem retornar MAPI_E_BAD_CHARWIDTH se MAPI_UNICODE é passado. 
  
## <a name="mfcmapi-reference"></a>Referência do MFCMAPI

Para ver códigos de exemplo do MFCMAPI, confira a tabela a seguir.
  
|**Arquivo**|**Função**|**Comentário**|
|:-----|:-----|:-----|
|FolderDlg. cpp  <br/> |CFolderDlg:: OnSelectForm  <br/> |MFCMAPI usa o método **IMAPIFormMgr:: SelectForm** para selecionar um formulário e enviar informações sobre o formulário para um ou mais logs.  <br/> |
   
## <a name="see-also"></a>Confira também



[IMAPIFormMgr : IUnknown](imapiformmgriunknown.md)


[MFCMAPI como exemplo de código](mfcmapi-as-a-code-sample.md)

