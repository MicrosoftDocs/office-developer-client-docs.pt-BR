---
title: IMAPIMessageSiteGetStore
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIMessageSite.GetStore
api_type:
- COM
ms.assetid: d1ca619e-8bdc-417b-aed6-23dd30e6eafa
description: '�ltima altera��o: segunda-feira, 9 de mar�o de 2015'
ms.openlocfilehash: 2787150a9fa0fc41e04c58b4a4310ffa844f3743
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19767088"
---
# <a name="imapimessagesitegetstore"></a>IMAPIMessageSite::GetStore

  
  
**Aplica-se a**: Outlook 
  
Retorna o repositório de mensagem que contém a mensagem atual, se existir um repositório tal. Este método retornará NULL no parâmetro _ppStore_ mensagens incorporado, o que são armazenados em outra mensagem em vez de diretamente em um repositório de mensagem. 
  
```cpp
HRESULT GetStore(
  LPMDB FAR * ppStore
);
```

## <a name="parameters"></a>Par�metros

 _ppStore_
  
> [out] Um ponteiro para um ponteiro para o armazenamento de mensagens.
    
## <a name="return-value"></a>Valor retornado

S_OK 
  
> A chamada foi bem-sucedida e retornou o valor esperado ou valores.
    
S_FALSE 
  
> Não há nenhum repositório que contém a mensagem.
    
## <a name="remarks"></a>Coment�rios

Para obter uma lista das interfaces relacionadas aos servidores de formulário, consulte [Interfaces de formulário de MAPI](mapi-form-interfaces.md).
  
## <a name="mfcmapi-reference"></a>Referência MFCMAPI

Para exemplos de código MFCMAPI, consulte a tabela a seguir.
  
|**Arquivo**|**Function**|**Comment**|
|:-----|:-----|:-----|
|MyMAPIFormViewer.cpp  <br/> |CMyMAPIFormViewer::GetStore  <br/> |MFCMAPI usa o método **IMAPIMessageSite::GetStore** para obter o ponteiro atualmente em cache para o repositório especificado, se ele estiver disponível.  <br/> |
   
## <a name="see-also"></a>Confira também



[IMAPIMessageSite: IUnknown](imapimessagesiteiunknown.md)


[MFCMAPI como um exemplo de código](mfcmapi-as-a-code-sample.md)
  
[Interfaces de formulário MAPI](mapi-form-interfaces.md)

