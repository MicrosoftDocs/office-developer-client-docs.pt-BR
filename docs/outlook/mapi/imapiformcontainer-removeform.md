---
title: IMAPIFormContainerRemoveForm
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIFormContainer.RemoveForm
api_type:
- COM
ms.assetid: 7f851ce8-bd01-4ea5-86e0-e44323cc0aab
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: 0d2c908f86ccd66ffd3a2eb2506d129ee2a14d48
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19767011"
---
# <a name="imapiformcontainerremoveform"></a>IMAPIFormContainer::RemoveForm

  
  
**Aplica-se a**: Outlook 
  
Remove um determinado formulário de um contêiner de formulário.
  
```cpp
HRESULT RemoveForm(
  LPCSTR szMessageClass
);
```

## <a name="parameters"></a>Parâmetros

 _szMessageClass_
  
> [in] Uma cadeia de caracteres que nomeia a classe de mensagem do formulário a ser removido do contêiner do formulário. Nomes de classe de mensagem são sempre cadeias de caracteres ANSI, Unicode nunca.
    
## <a name="return-value"></a>Valor retornado

S_OK 
  
> A chamada foi bem-sucedida e retornou o valor esperado ou valores.
    
E_NOT_FOUND 
  
> A classe de mensagem passada no parâmetro _szMessageClass_ não coincide com a classe de mensagem de qualquer formulário no contêiner do formulário. 
    
## <a name="mfcmapi-reference"></a>Referência MFCMAPI

Para exemplos de código MFCMAPI, consulte a tabela a seguir.
  
|**Arquivo**|**Function**|**Comment**|
|:-----|:-----|:-----|
|FormContainerDlg.cpp  <br/> |CFormContainerDlg::OnDeleteSelectedItem  <br/> |MFCMAPI usa o método **IMAPIFormContainer::RemoveForm** para excluir um formulário de um contêiner de formulário.  <br/> |
   
## <a name="see-also"></a>Confira também



[IMAPIFormContainer : IUnknown](imapiformcontaineriunknown.md)


[MFCMAPI como um exemplo de código](mfcmapi-as-a-code-sample.md)

