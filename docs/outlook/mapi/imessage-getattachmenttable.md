---
title: IMessageGetAttachmentTable
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMessage.GetAttachmentTable
api_type:
- COM
ms.assetid: e568917e-6085-4094-8728-89ba90a78c40
description: '�ltima altera��o: s�bado, 23 de julho de 2011'
ms.openlocfilehash: bf100ed916080a91366062f45b9e3349516bdb98
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22588514"
---
# <a name="imessagegetattachmenttable"></a>IMessage::GetAttachmentTable

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Retorna a tabela de anexos da mensagem.
  
```cpp
HRESULT GetAttachmentTable(
  ULONG ulFlags,
  LPMAPITABLE FAR * lppTable
);
```

## <a name="parameters"></a>Parâmetros

 _ulFlags_
  
> [in] Bitmask dos sinalizadores que se relacionam com a criação da tabela. O seguinte sinalizador pode ser definido: 
    
MAPI_UNICODE 
  
> As colunas de cadeia de caracteres estão no formato Unicode. Se o sinalizador MAPI_UNICODE não estiver definido, as colunas de cadeia de caracteres estão no formato ANSI.
    
MAPI_DEFERRED_ERRORS 
  
> Permite que **GetAttachmentTable** retornar com êxito, possivelmente antes que a tabela é totalmente disponível para o cliente da chamada. Se a tabela não estiver disponível, fazendo uma chamada subsequente a ele pode causar um erro. 
    
 _lppTable_
  
> [out] Ponteiro para um ponteiro para a tabela de anexos.
    
## <a name="return-value"></a>Valor retornado

S_OK 
  
> A tabela de anexo foi recuperada com êxito.
    
## <a name="remarks"></a>Comentários

O método **IMessage::GetAttachmentTable** retorna um ponteiro para a tabela de anexos da mensagem, que inclui informações sobre todos os anexos da mensagem. Os clientes podem obter acesso a um anexo através de apenas a tabela de anexos. Recuperando o número de um anexo sua propriedade **PR_ATTACH_NUM** ([PidTagAttachNumber](pidtagattachnumber-canonical-property.md)) um cliente pode usar vários métodos **IMessage** para trabalhar com o anexo. 
  
Não há uma linha para cada anexo. Para obter uma lista completa das colunas em uma tabela de anexo, consulte [As tabelas de anexo](attachment-tables.md).
  
Um anexo normalmente não aparecem na tabela anexo até que o anexo e a mensagem foram salvos com uma chamada para [IMAPIProp::SaveChanges](imapiprop-savechanges.md). Tabelas do anexo são dinâmicas. Se um cliente cria um novo anexo, exclui um anexo existente ou altera um ou mais propriedades depois que as chamadas **SaveChanges** foram feitas no anexo na mensagem, a tabela de anexo será atualizada para refletir as novas informações. 
  
Suportam a uma ampla variedade de restrições; algumas tabelas de anexo outros não. Suporte a restrições depende da implementação do provedor de repositório de mensagem. 
  
Quando aberto inicialmente, tabelas de anexo não são necessariamente classificadas em alguma ordem específica. 
  
Definir o sinalizador MAPI_UNICODE no parâmetro _ulFlags_ afeta as seguintes chamadas à tabela de anexo: 
  
- [IMAPITable::QueryColumns](imapitable-querycolumns.md) para recuperar o conjunto de coluna. 
    
- [IMAPITable:: QueryRows](imapitable-queryrows.md) para recuperar linhas. 
    
- [IMAPITable::QuerySortOrder](imapitable-querysortorder.md) para recuperar a ordem de classificação. 
    
Definindo as solicitações de sinalizador Unicode que as informações de quaisquer colunas de cadeia de caracteres retornada dessas chamadas estar no formato Unicode. No entanto, porque nem todos os provedores de armazenamento de mensagem oferecem suporte a Unicode, defina esse sinalizador é apenas uma solicitação.
  
## <a name="see-also"></a>Confira também



[IMessage::CreateAttach](imessage-createattach.md)
  
[IMessage::DeleteAttach](imessage-deleteattach.md)
  
[IMessage::OpenAttach](imessage-openattach.md)
  
[IMessage : IMAPIProp](imessageimapiprop.md)

