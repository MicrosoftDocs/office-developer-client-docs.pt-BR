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
description: 'Última modificação: 23 de julho de 2011'
ms.openlocfilehash: 9a77d335f3c8980de29dab6e14079c83bd711b43
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33421169"
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
  
> [in] Bitmask de sinalizadores relacionados à criação da tabela. O sinalizador a seguir pode ser definido: 
    
MAPI_UNICODE 
  
> As colunas de cadeia de caracteres estão no formato Unicode. Se o MAPI_UNICODE não estiver definido, as colunas de cadeia de caracteres estão no formato ANSI.
    
MAPI_DEFERRED_ERRORS 
  
> Permite que **GetAttachmentTable** retorne com êxito, possivelmente antes da tabela estar totalmente disponível para o cliente de chamada. Se a tabela não estiver disponível, fazer uma chamada subsequente pode causar um erro. 
    
 _lppTable_
  
> [out] Ponteiro para um ponteiro para a tabela de anexos.
    
## <a name="return-value"></a>Valor de retorno

S_OK 
  
> A tabela de anexos foi recuperada com êxito.
    
## <a name="remarks"></a>Comentários

O **método IMessage::GetAttachmentTable** retorna um ponteiro para a tabela de anexos da mensagem, que inclui informações sobre todos os anexos na mensagem. Os clientes só podem obter acesso a um anexo por meio da tabela de anexos. Ao recuperar o número de um anexo, sua propriedade **PR_ATTACH_NUM** ([PidTagAttachNumber](pidtagattachnumber-canonical-property.md)) de um cliente pode usar vários dos métodos **IMessage** para trabalhar com o anexo. 
  
Há uma linha para cada anexo. Para uma lista completa das colunas em uma tabela de anexos, consulte [Attachment Tables](attachment-tables.md).
  
Um anexo geralmente não aparece na tabela de anexos até que o anexo e a mensagem tenham sido salvos com uma chamada para [IMAPIProp::SaveChanges](imapiprop-savechanges.md). As tabelas de anexos são dinâmicas. Se um cliente cria um novo anexo, exclui um anexo existente ou altera uma ou mais propriedades depois que as chamadas **SaveChanges** são feitas no anexo na mensagem, a tabela de anexos será atualizada para refletir as novas informações. 
  
Algumas tabelas de anexos suportam uma ampla variedade de restrições; outras não fazem isso. O suporte para restrições depende da implementação do provedor do armazenamento de mensagens. 
  
Quando abertas inicialmente, as tabelas de anexos não são necessariamente ordenadas em uma ordem específica. 
  
A definição MAPI_UNICODE sinalizador de configuração no  _parâmetro ulFlags_ afeta as seguintes chamadas para a tabela de anexos: 
  
- [IMAPITable::QueryColumns](imapitable-querycolumns.md) para recuperar o conjunto de colunas. 
    
- [IMAPITable::QueryRows](imapitable-queryrows.md) para recuperar linhas. 
    
- [IMAPITable::QuerySortOrder](imapitable-querysortorder.md) para recuperar a ordem de classificação. 
    
A configuração do sinalizador Unicode solicita que as informações de quaisquer colunas de cadeia de caracteres retornadas dessas chamadas sejam no formato Unicode. No entanto, como nem todos os provedores de armazenamento de mensagens suportam Unicode, definir esse sinalizador é apenas uma solicitação.
  
## <a name="see-also"></a>Confira também



[IMessage::CreateAttach](imessage-createattach.md)
  
[IMessage::DeleteAttach](imessage-deleteattach.md)
  
[IMessage::OpenAttach](imessage-openattach.md)
  
[IMessage : IMAPIProp](imessageimapiprop.md)

