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
ms.openlocfilehash: e53c0cbd9946ff04516594a7ce99fdc2daf4ff4d
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32355738"
---
# <a name="imapiformcontainerremoveform"></a>IMAPIFormContainer::RemoveForm

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Remove um formulário específico de um contêiner de formulários.
  
```cpp
HRESULT RemoveForm(
  LPCSTR szMessageClass
);
```

## <a name="parameters"></a>Parâmetros

 _szMessageClass_
  
> no Uma cadeia de caracteres que nomeia a classe de mensagem do formulário a ser removido do contêiner de formulários. Os nomes de classe de mensagem são sempre cadeias de caracteres ANSI, nunca Unicode.
    
## <a name="return-value"></a>Valor de retorno

S_OK 
  
> A chamada teve êxito e retornou o valor ou valores esperados.
    
MAPI_E_NOT_FOUND 
  
> A classe de mensagem passada no parâmetro _szMessageClass_ não corresponde à classe de mensagem de qualquer formulário no contêiner de formulários. 
    
## <a name="mfcmapi-reference"></a>Referência do MFCMAPI

Para ver códigos de exemplo do MFCMAPI, confira a tabela a seguir.
  
|**Arquivo**|**Função**|**Comentário**|
|:-----|:-----|:-----|
|FormContainerDlg. cpp  <br/> |CFormContainerDlg:: OnDeleteSelectedItem  <br/> |MFCMAPI usa o método **IMAPIFormContainer:: RemoveForm** para excluir um formulário de um contêiner de formulários.  <br/> |
   
## <a name="see-also"></a>Confira também



[IMAPIFormContainer : IUnknown](imapiformcontaineriunknown.md)


[MFCMAPI como exemplo de código](mfcmapi-as-a-code-sample.md)

