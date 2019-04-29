---
title: IMAPIContainer IMAPIProp
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIContainer
api_type:
- COM
ms.assetid: d83fdd83-3e86-43c8-a73f-8e9e01b53371
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: 8be3b1857d539f81e42d2ac3e5813afa73513a16
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33406119"
---
# <a name="imapicontainer--imapiprop"></a>IMAPIContainer : IMAPIProp

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Gerencia operações de alto nível em objetos de contêiner, como catálogos de endereços, listas de distribuição e pastas. As interfaces [IMAPIFolder: IMAPIContainer](imapifolderimapicontainer.md), [IABContainer: IMAPIContainer](iabcontainerimapicontainer.md)e [IDistList: IMAPIContainer](idistlistimapicontainer.md) são derivadas de **IMAPIContainer**.
  
|||
|:-----|:-----|
|Arquivo de cabeçalho:  <br/> |Mapidefs. h  <br/> |
|Exposto por:  <br/> |Pastas, contêiner de catálogo de endereços e objetos de lista de distribuição  <br/> |
|Implementado por:  <br/> |Repositório de mensagens, catálogo de endereços e provedores de transporte remoto  <br/> |
|Chamado por:  <br/> |Aplicativos cliente  <br/> |
|Identificador de interface:  <br/> |IID_IMAPIContainer  <br/> |
|Tipo de ponteiro:  <br/> |LPMAPICONTAINER  <br/> |
|Modelo de transação:  <br/> |Classe abstrata, nunca implementado  <br/> |
   
## <a name="vtable-order"></a>Vtable order

|||
|:-----|:-----|
|[GetContenttable](imapicontainer-getcontentstable.md) <br/> |Retorna um ponteiro para a tabela de conteúdo do contêiner.  <br/> |
|[GetHierarchytable](imapicontainer-gethierarchytable.md) <br/> |Retorna um ponteiro para a tabela de hierarquia do contêiner.  <br/> |
|[OpenEntry](imapicontainer-openentry.md) <br/> |Abre um objeto no contêiner, retornando um ponteiro de interface para acesso adicional.  <br/> |
|[SetSearchCriteria](imapicontainer-setsearchcriteria.md) <br/> |Estabelece critérios de pesquisa para o contêiner.  <br/> |
|[GetSearchCriteria](imapicontainer-getsearchcriteria.md) <br/> |Obtém os critérios de pesquisa para o contêiner.  <br/> |
   
|**Propriedades necessárias**|**Acesso**|
|:-----|:-----|
|**PR_CONTAINER_HIERARCHY** ([PidTagContainerHierarchy](pidtagcontainerhierarchy-canonical-property.md))  <br/> |Somente leitura  <br/> |
|**PR_CONTAINER_CONTENTS** ([PidTagContainerContents](pidtagcontainercontents-canonical-property.md))  <br/> |Somente leitura  <br/> |
|**PR_CONTAINER_FLAGS** ([PidTagContainerFlags](pidtagcontainerflags-canonical-property.md))  <br/> |Leitura/gravação  <br/> |
   
## <a name="see-also"></a>Confira também



[Interfaces MAPI](mapi-interfaces.md)

