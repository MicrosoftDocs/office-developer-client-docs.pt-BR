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
description: '�ltima altera��o: segunda-feira, 9 de mar�o de 2015'
ms.openlocfilehash: 0f9826dab72968055604c5bb9f8f537facc5618e
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19767029"
---
# <a name="imapiformcontainergetdisplay"></a>IMAPIFormContainer::GetDisplay

  
  
**Aplica-se a**: Outlook 
  
Retorna o nome de exibição de um contêiner de formulário.
  
```cpp
HRESULT GetDisplay(
  ULONG ulFlags,
  LPSTR FAR * pszDisplayName
);
```

## <a name="parameters"></a>Par�metros

 _ulFlags_
  
> [in] Uma bitmask dos sinalizadores que controla o tipo de cadeia de caracteres retornada. O seguinte sinalizador pode ser definido:
    
MAPI_UNICODE 
  
> A cadeia de caracteres retornada está no formato Unicode. Se o sinalizador MAPI_UNICODE não estiver definido, a cadeia de caracteres é no formato ANSI.
    
 _pszDisplayName_
  
> [out] Um ponteiro para uma cadeia de caracteres que contém o nome de exibição do contêiner do formulário.
    
## <a name="return-value"></a>Valor retornado

S_OK 
  
> A chamada foi bem-sucedida e retornou o valor esperado ou valores.
    
## <a name="mfcmapi-reference"></a>Referência MFCMAPI

Para exemplos de código MFCMAPI, consulte a tabela a seguir.
  
|**Arquivo**|**Function**|**Comment**|
|:-----|:-----|:-----|
|FormContainerDlg.cpp  <br/> |CFormContainerDlg::CFormContainerDlg  <br/> |MFCMAPI usa o método **IMAPIFormContainer::GetDisplay** para obter o nome do contêiner formulário quando ele for processada CFormContainerDlg.  <br/> |
   
## <a name="see-also"></a>Confira também



[IMAPIFormContainer: IUnknown](imapiformcontaineriunknown.md)


[MFCMAPI como um exemplo de código](mfcmapi-as-a-code-sample.md)

