---
title: ITableData IUnknown
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- ITableData
api_type:
- COM
ms.assetid: ac7ae09f-ce19-45cf-8963-fad5bba75452
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: 3992bea899239ee5975505dec366490d6bbe1698
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33430592"
---
# <a name="itabledata--iunknown"></a>ITableData : IUnknown

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Fornece métodos utilitários para trabalhar com tabelas. MAPI provides table data objects or objects that implement **ITableData** to help service providers perform table maintenance. Para obter um objeto de dados de tabela, os provedores de serviços chamam a [função CreateTable.](createtable.md) 
  
|||
|:-----|:-----|
|Arquivo de cabeçalho:  <br/> |Mapiutil.h  <br/> |
|Exposto por:  <br/> |Objetos de dados de tabela  <br/> |
|Implementado por:  <br/> |MAPI  <br/> |
|Chamado por:  <br/> |Provedores de serviços  <br/> |
|Identificador de interface:  <br/> |IID_IMAPITableData  <br/> |
|Tipo de ponteiro:  <br/> |LPTABLEDATA  <br/> |
   
## <a name="vtable-order"></a>Vtable order

|||
|:-----|:-----|
|[HrGetView](itabledata-hrgetview.md) <br/> |Cria um exibição de tabela, retornando um ponteiro para uma [implementação IMAPITable.](imapitableiunknown.md)  <br/> |
|[HrModifyRow](itabledata-hrmodifyrow.md) <br/> |Insere uma nova linha de tabela, possivelmente substituindo uma linha existente.  <br/> |
|[HrDeleteRow](itabledata-hrdeleterow.md) <br/> |Exclui uma linha de tabela.  <br/> |
|[HrQueryRow](itabledata-hrqueryrow.md) <br/> |Recupera uma linha de tabela.  <br/> |
|[HrEnumRow](itabledata-hrenumrow.md) <br/> |Recupera uma linha com base em sua posição na tabela.  <br/> |
|[HrNotify](itabledata-hrnotify.md) <br/> |Envia uma notificação para uma linha de tabela.  <br/> |
|[HrInsertRow](itabledata-hrinsertrow.md) <br/> |Insere uma linha de tabela.  <br/> |
|[HrModifyRows](itabledata-hrmodifyrows.md) <br/> |Insere várias linhas de tabela, possivelmente substituindo linhas existentes.  <br/> |
|[HrDeleteRows](itabledata-hrdeleterows.md) <br/> |Exclui várias linhas de tabela.  <br/> |
   
## <a name="remarks"></a>Comentários

A implementação de MAPI de **ITableData** funciona com tabelas, mantendo todos os dados e quaisquer restrições associadas na memória, tornando-a inadequada para uso com tabelas muito grandes. Não há suporte para restrições grandes e operações complexas, como categorização. 
  
Os objetos de dados de tabela identificam linhas usando uma coluna de índice, uma propriedade que tem garantia de ter um valor exclusivo para cada linha. A maioria dos provedores de serviços **usa PR_INSTANCE_KEY** propriedade ([PidTagInstanceKey](pidtaginstancekey-canonical-property.md)) como a coluna de índice. Propriedades com vários valores não podem ser usadas como uma coluna de índice.
  
Os objetos de dados de tabela geram uma única notificação, independentemente do número de linhas afetadas por uma alteração ou exclusão. Se uma linha de destino em uma operação não existir, uma linha será adicionada.
  
## <a name="see-also"></a>Confira também



[Interfaces MAPI](mapi-interfaces.md)

