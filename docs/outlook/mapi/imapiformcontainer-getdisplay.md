---
title: IMAPIFormContainerGetDisplay
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIFormContainer.GetDisplay
api_type:
- COM
ms.assetid: 6829e273-4a75-4278-b58a-ae7543e075ac
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: 994041d050df56fd3fa3c0e599542e05a202ad65
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33416129"
---
# <a name="imapiformcontainergetdisplay"></a>IMAPIFormContainer::GetDisplay

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Retorna o nome de exibição de um contêiner de formulário.
  
```cpp
HRESULT GetDisplay(
  ULONG ulFlags,
  LPSTR FAR * pszDisplayName
);
```

## <a name="parameters"></a>Parâmetros

 _ulFlags_
  
> [in] Uma máscara de bits de sinalizadores que controla o tipo da cadeia de caracteres retornada. O sinalizador a seguir pode ser definido:
    
MAPI_UNICODE 
  
> A cadeia de caracteres retornada está no formato Unicode. Se o MAPI_UNICODE não estiver definido, a cadeia de caracteres está no formato ANSI.
    
 _pszDisplayName_
  
> [out] Um ponteiro para uma cadeia de caracteres que contém o nome de exibição do contêiner de formulário.
    
## <a name="return-value"></a>Valor de retorno

S_OK 
  
> A chamada foi bem-sucedida e retornou o valor ou os valores esperados.
    
## <a name="mfcmapi-reference"></a>Referência do MFCMAPI

Para ver códigos de exemplo do MFCMAPI, confira a tabela a seguir.
  
|**Arquivo**|**Função**|**Comentário**|
|:-----|:-----|:-----|
|FormContainerDlg.cpp  <br/> |CFormContainerDlg::CFormContainerDlg  <br/> |MFCMAPI uses the **IMAPIFormContainer::GetDisplay** method to get the name of the form container when it renders CFormContainerDlg.  <br/> |
   
## <a name="see-also"></a>Confira também



[IMAPIFormContainer : IUnknown](imapiformcontaineriunknown.md)


[MFCMAPI como exemplo de código](mfcmapi-as-a-code-sample.md)

