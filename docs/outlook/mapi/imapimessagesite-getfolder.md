---
title: IMAPIMessageSiteGetFolder
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIMessageSite.GetFolder
api_type:
- COM
ms.assetid: 9f4b4147-ed98-47cb-a799-ddf028f8e826
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: 24461099877af683109c8627eacd22a657d6e156
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33430564"
---
# <a name="imapimessagesitegetfolder"></a>IMAPIMessageSite::GetFolder

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Retorna a pasta na qual a mensagem atual foi criada ou aberta, se essa pasta existir. Este método retorna NULL no parâmetro _ppFolder_ para mensagens incorporadas, que não são armazenadas diretamente em uma pasta. 
  
```cpp
HRESULT GetFolder(
  LPMAPIFOLDER FAR * ppFolder
);
```

## <a name="parameters"></a>Parâmetros

 _ppFolder_
  
> bota Um ponteiro para um ponteiro para a pasta retornada.
    
## <a name="return-value"></a>Valor de retorno

S_OK 
  
> A chamada teve êxito e retornou o valor ou valores esperados.
    
S_FALSE 
  
> Nenhuma pasta existe para a mensagem.
    
## <a name="remarks"></a>Comentários

Para obter uma lista de interfaces relacionadas a servidores de formulário, consulte [interfaces de formulários MAPI](mapi-form-interfaces.md).
  
## <a name="mfcmapi-reference"></a>Referência do MFCMAPI

Para ver códigos de exemplo do MFCMAPI, confira a tabela a seguir.
  
|**Arquivo**|**Função**|**Comentário**|
|:-----|:-----|:-----|
|MyMAPIFormViewer. cpp  <br/> |CMyMAPIFormViewer:: getFolder  <br/> |MFCMAPI usa o método **IMAPIMessageSite:: GetFolder** para retornar o ponteiro em cache atualmente para a pasta especificada.  <br/> |
   
## <a name="see-also"></a>Confira também



[IMAPIMessageSite : IUnknown](imapimessagesiteiunknown.md)


[MFCMAPI como exemplo de código](mfcmapi-as-a-code-sample.md)
  
[Interfaces de formulário MAPI](mapi-form-interfaces.md)

