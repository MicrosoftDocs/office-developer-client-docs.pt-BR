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
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33423577"
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
  
> [in] Um alça para a janela pai da caixa de diálogo exibida. 
    
 _ulFlags_
  
> [in] Uma máscara de bits de sinalizadores que controla o tipo das cadeias de caracteres passadas. O sinalizador a seguir pode ser definido:
    
MAPI_UNICODE 
  
> As cadeias de caracteres passadas estão no formato Unicode. Se o MAPI_UNICODE não estiver definido, as cadeias de caracteres estão no formato ANSI.
    
 _pszTitle_
  
> [in] Um ponteiro para uma cadeia de caracteres que contém a legenda da caixa de diálogo. Se o  _parâmetro pszTitle_ for NULL, o provedor da biblioteca de formulário fornece uma legenda padrão. 
    
 _pfld_
  
> [in] Um ponteiro para a pasta a partir da qual o formulário deve ser selecionado. Se o  _parâmetro pfld_ for NULL, o formulário poderá ser selecionado no contêiner de formulário local, pessoal ou da organização. 
    
 _ppfrminfoReturned_
  
> [out] Um ponteiro para um ponteiro para o objeto de informações de formulário retornado.
    
## <a name="return-value"></a>Valor de retorno

S_OK 
  
> A chamada foi bem-sucedida e retornou o valor ou os valores esperados.
    
MAPI_E_BAD_CHARWIDTH 
  
> O sinalizador MAPI_UNICODE foi definido e a implementação não dá suporte a Unicode ou MAPI_UNICODE não foi definido e a implementação dá suporte apenas a Unicode.
    
MAPI_E_USER_CANCEL 
  
> O usuário cancelou a operação, normalmente clicando no botão **Cancelar** na caixa de diálogo. 
    
## <a name="remarks"></a>Comentários

Visualizadores de formulário chamam o método **IMAPIFormMgr::SelectForm** para apresentar primeiro uma caixa de diálogo que permite ao usuário selecionar um formulário e, em seguida, recuperar um objeto de informações de formulário que descreve o formulário selecionado. A caixa de diálogo restringe o usuário a selecionar um único formulário. 
  
## <a name="notes-to-callers"></a>Notas para chamadores

A **caixa de diálogo SelectForm** exibe somente formulários que não estão ocultos (ou seja, formulários que têm suas propriedades ocultas claras). Se um visualizador de formulário passar o sinalizador MAPI_UNICODE no  _parâmetro ulFlags,_ todas as cadeias de caracteres serão Unicode. Provedores de biblioteca de formulário que não suportam cadeias de caracteres Unicode devem retornar MAPI_E_BAD_CHARWIDTH se MAPI_UNICODE for passado. 
  
## <a name="mfcmapi-reference"></a>Referência do MFCMAPI

Para ver códigos de exemplo do MFCMAPI, confira a tabela a seguir.
  
|**Arquivo**|**Função**|**Comentário**|
|:-----|:-----|:-----|
|FolderDlg.cpp  <br/> |CFolderDlg::OnSelectForm  <br/> |MFCMAPI usa o **método IMAPIFormMgr::SelectForm** para selecionar um formulário e enviar informações sobre o formulário para um ou mais logs.  <br/> |
   
## <a name="see-also"></a>Confira também



[IMAPIFormMgr : IUnknown](imapiformmgriunknown.md)


[MFCMAPI como exemplo de código](mfcmapi-as-a-code-sample.md)

