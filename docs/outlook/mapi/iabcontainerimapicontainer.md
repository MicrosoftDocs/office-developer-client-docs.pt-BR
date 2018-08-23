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
ms.openlocfilehash: 519093b3c538037b5a42bc19cc65ed31ae19f07b
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22580702"
---
# <a name="iabcontainer--imapicontainer"></a>IABContainer : IMAPIContainer

**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Fornece acesso aos contêineres do catálogo de endereços. Aplicativos MAPI e cliente chamam os métodos de **IABContainer** para realizar a resolução de nomes e para criar, copiar e exclua os destinatários. 
  
|||
|:-----|:-----|
|Arquivo de cabeçalho:  <br/> |Mapidefs.h  <br/> |
|Expostos pelo:  <br/> |Objetos de contêiner de catálogo de endereços  <br/> |
|Implementada por:  <br/> |Provedores de catálogo de endereços  <br/> |
|Chamado pelo:  <br/> |Aplicativos MAPI e cliente  <br/> |
|Identificador de interface:  <br/> |IID_IABContainer  <br/> |
|Tipo de ponteiro:  <br/> |LPABCONT  <br/> |
|Modelo de transação:  <br/> |Transacionadas  <br/> |
   
## <a name="vtable-order"></a>Ordem vtable

|||
|:-----|:-----|
|[CreateEntry](iabcontainer-createentry.md) <br/> |Cria uma nova entrada, que pode ser um usuário de mensagens, uma lista de distribuição ou outro contêiner.  <br/> |
|[CopyEntries](iabcontainer-copyentries.md) <br/> |Copia uma ou mais entradas, os usuários geralmente mensagens ou listas de distribuição.  <br/> |
|[DeleteEntries](iabcontainer-deleteentries.md) <br/> |Remove uma ou mais entradas, normalmente mensagens outros contêineres, listas de distribuição ou os usuários.  <br/> |
|[ResolveNames](iabcontainer-resolvenames.md) <br/> |Executa a resolução de nomes para uma ou mais entradas de destinatário.  <br/> |
   
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

A interface **IABContainer** herda indiretamente da interface [IUnknown](http://msdn.microsoft.com/en-us/library/ms680509%28VS.85%29.aspx) por meio do [IMAPIContainer: IMAPIProp](imapicontainerimapiprop.md) e [IMAPIProp: IUnknown](imapipropiunknown.md) interfaces. Provedores de catálogo de endereços implementam a interface de **IABContainer** . 
  
Qualquer número de objetos de usuário de mensagens, listas de distribuição e outros contêineres do catálogo de endereços pode existir em um contêiner de catálogo de endereços. Assim como acontece com qualquer contêiner, clientes ou provedores de serviços podem usar um contêiner de catálogo de endereços para abrir uma das suas entradas ou para recuperar uma tabela de hierarquia ou a tabela de conteúdo. Contêineres também fornecem resolução de nomes e, dependendo de provedor, a capacidade de adicionar, remover ou modificar entradas de catálogo de endereços.
  
MAPI define um contêiner de catálogo de endereços especial chamado o catálogo de endereços pessoal (PAB) que contém as entradas copiadas de outros contêineres. Um PAB sempre é modificável. Os usuários preenchem geralmente seu PAB com entradas designar os destinatários com o qual se comunicam com mais frequência. Um PAB também pode manter endereços únicos e novos destinatários ainda não parte de qualquer contêiner de catálogo de endereços.
  
## <a name="see-also"></a>Confira também

- [Interfaces MAPI](mapi-interfaces.md)

