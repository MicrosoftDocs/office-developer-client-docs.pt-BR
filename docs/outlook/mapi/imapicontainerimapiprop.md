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
description: '�ltima altera��o: segunda-feira, 9 de mar�o de 2015'
ms.openlocfilehash: e24f5ebd73a4652876282099f1460762c150b94d
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19766947"
---
# <a name="imapicontainer--imapiprop"></a>IMAPIContainer: IMAPIProp

  
  
**Aplica-se a**: Outlook 
  
Gerencia as operações de alto nível em objetos de contêiner como catálogos de endereços, pastas e listas de distribuição. O [IMAPIFolder: IMAPIContainer](imapifolderimapicontainer.md), [IABContainer: IMAPIContainer](iabcontainerimapicontainer.md), e [IDistList: IMAPIContainer](idistlistimapicontainer.md) interfaces são derivados do **IMAPIContainer**.
  
|||
|:-----|:-----|
|Arquivo de cabeçalho:  <br/> |Mapidefs.h  <br/> |
|Expostos pelo:  <br/> |Pasta, o contêiner de catálogo de endereços e objetos de lista de distribuição  <br/> |
|Implementada por:  <br/> |Armazenamento de mensagens, catálogo de endereços e provedores de transporte remoto  <br/> |
|Chamado pelo:  <br/> |Aplicativos cliente  <br/> |
|Identificador de interface:  <br/> |IID_IMAPIContainer  <br/> |
|Tipo de ponteiro:  <br/> |LPMAPICONTAINER  <br/> |
|Modelo de transação:  <br/> |Classe abstrata, nunca implementada  <br/> |
   
## <a name="vtable-order"></a>Ordem vtable

|||
|:-----|:-----|
|[GetContentsTable](imapicontainer-getcontentstable.md) <br/> |Retorna um ponteiro para a tabela de conteúdo do contêiner.  <br/> |
|[GetHierarchyTable](imapicontainer-gethierarchytable.md) <br/> |Retorna um ponteiro para a tabela de hierarquia do contêiner.  <br/> |
|[OpenEntry](imapicontainer-openentry.md) <br/> |Abre um objeto no contêiner, retornando um ponteiro de interface para obter mais acesso.  <br/> |
|[Definir SetSearchCriteria](imapicontainer-setsearchcriteria.md) <br/> |Estabelece os critérios de pesquisa para o contêiner.  <br/> |
|[Obter GetSearchCriteria](imapicontainer-getsearchcriteria.md) <br/> |Obtém os critérios de pesquisa para o contêiner.  <br/> |
   
|**Propriedades necessárias**|**Access**|
|:-----|:-----|
|**PR_CONTAINER_HIERARCHY** ([PidTagContainerHierarchy](pidtagcontainerhierarchy-canonical-property.md))  <br/> |Somente leitura  <br/> |
|**PR_CONTAINER_CONTENTS** ([PidTagContainerContents](pidtagcontainercontents-canonical-property.md))  <br/> |Somente leitura  <br/> |
|**PR_CONTAINER_FLAGS** ([PidTagContainerFlags](pidtagcontainerflags-canonical-property.md))  <br/> |Leitura/gravação  <br/> |
   
## <a name="see-also"></a>Confira também



[Interfaces MAPI](mapi-interfaces.md)

