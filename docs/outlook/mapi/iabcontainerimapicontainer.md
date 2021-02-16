---
title: IABContainer IMAPIContainer
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IABContainer
api_type:
- COM
ms.assetid: 1f5ce6e0-b79a-4da2-b014-8c00cd72912e
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: 0905fbe2ba584aef49c50152aaf448267d477c10
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32348955"
---
# <a name="iabcontainer--imapicontainer"></a>IABContainer : IMAPIContainer

**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Fornece acesso a contêineres do livro de endereços. MapI and client applications call the methods of **IABContainer** to perform name resolution and to create, copy, and delete recipients. 
  
|||
|:-----|:-----|
|Arquivo de cabeçalho:  <br/> |Mapidefs.h  <br/> |
|Exposto por:  <br/> |Objetos de contêiner do livro de endereços  <br/> |
|Implementado por:  <br/> |Provedores de lista de endereços  <br/> |
|Chamado por:  <br/> |MAPI e aplicativos cliente  <br/> |
|Identificador de interface:  <br/> |IID_IABContainer  <br/> |
|Tipo de ponteiro:  <br/> |LPABCONT  <br/> |
|Modelo de transação:  <br/> |Transacted  <br/> |
   
## <a name="vtable-order"></a>Vtable order

|||
|:-----|:-----|
|[CreateEntry](iabcontainer-createentry.md) <br/> |Cria uma nova entrada, que pode ser um usuário de mensagens, uma lista de distribuição ou outro contêiner.  <br/> |
|[CopyEntries](iabcontainer-copyentries.md) <br/> |Copia uma ou mais entradas, normalmente usuários de mensagens ou listas de distribuição.  <br/> |
|[DeleteEntries](iabcontainer-deleteentries.md) <br/> |Remove uma ou mais entradas, normalmente usuários de mensagens, listas de distribuição ou outros contêineres.  <br/> |
|[ResolveNames](iabcontainer-resolvenames.md) <br/> |Executa a resolução de nome para uma ou mais entradas de destinatário.  <br/> |
   
|**Propriedades necessárias**|**Access**|
|:-----|:-----|
|**PR_CONTAINER_FLAGS** ([PidTagContainerFlags](pidtagcontainerflags-canonical-property.md))  <br/> |Leitura/gravação  <br/> |
|**PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md))  <br/> |Leitura/gravação  <br/> |
|**PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md))  <br/> |Somente leitura  <br/> |
|**PR_OBJECT_TYPE** ([PidTagObjectType](pidtagobjecttype-canonical-property.md))  <br/> |Somente leitura  <br/> |
|**PR_RECORD_KEY** ([PidTagRecordKey](pidtagrecordkey-canonical-property.md))  <br/> |Somente leitura  <br/> |
   
|**Propriedades opcionais**|**Access**|
|:-----|:-----|
|**PR_CONTAINER_CONTENTS** ([PidTagContainerContents](pidtagcontainercontents-canonical-property.md))  <br/> |Somente leitura  <br/> |
|**PR_CONTAINER_HIERARCHY** ([PidTagContainerHierarchy](pidtagcontainerhierarchy-canonical-property.md))  <br/> |Somente leitura  <br/> |
|**PR_DEF_CREATE_DL** ([PidTagDefCreateDl](pidtagdefcreatedl-canonical-property.md))  <br/> |Somente leitura  <br/> |
|**PR_DEF_CREATE_MAILUSER** ([PidTagDefCreateMailuser](pidtagdefcreatemailuser-canonical-property.md))  <br/> |Somente leitura  <br/> |
|**PR_DISPLAY_TYPE** ([PidTagDisplayType](pidtagdisplaytype-canonical-property.md))  <br/> |Somente leitura  <br/> |
   
## <a name="remarks"></a>Comentários

A interface **IABContainer** herda indiretamente da interface [IUnknown](https://msdn.microsoft.com/library/ms680509%28VS.85%29.aspx) por meio de [IMAPIContainer : IMAPIProp](imapicontainerimapiprop.md) e [IMAPIProp : interfaces IUnknown.](imapipropiunknown.md) Os provedores de agendas implementam a interface **IABContainer.** 
  
Qualquer número de objetos de usuário de mensagens, listas de distribuição e outros contêineres de listas de endereços pode existir em um contêiner de um livro de endereços. Como em qualquer contêiner, os clientes ou provedores de serviços podem usar um contêiner de livro de endereços para abrir uma de suas entradas ou para recuperar um índice de hierarquia ou de conteúdo. Os contêineres do livro de endereços também fornecem resolução de nomes e, dependendo do provedor, a capacidade de adicionar, remover ou modificar entradas.
  
MAPI define um contêiner de agenda especial chamado de pab (lista de endereços pessoal) que contém entradas copiadas de outros contêineres. Um PAB é sempre modificável. Os usuários geralmente preenchem sua PAB com entradas designando os destinatários com os quais eles se comunicam com mais frequência. Um PAB também pode manter endereços one-off e novos destinatários que ainda não fazem parte de qualquer contêiner do livro de endereços.
  
## <a name="see-also"></a>Confira também

- [Interfaces MAPI](mapi-interfaces.md)

