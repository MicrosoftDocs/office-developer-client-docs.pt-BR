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
ms.openlocfilehash: 968768fe75286b93bf12e349a4845fdfaa1923e9
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19767724"
---
# <a name="itabledata--iunknown"></a>ITableData : IUnknown

  
  
**Aplica-se a**: Outlook 
  
Fornece os métodos de utilitário para trabalhar com tabelas. MAPI fornece objetos de dados de tabela ou objetos que implementam **ITableData** para ajudar a executar manutenção da tabela de provedores de serviços. Para obter um objeto de dados de tabela, provedores de serviços de chamarem a função de [CreateTable](createtable.md) . 
  
|||
|:-----|:-----|
|Arquivo de cabeçalho:  <br/> |Mapiutil.h  <br/> |
|Expostos pelo:  <br/> |Objetos de dados de tabela  <br/> |
|Implementada por:  <br/> |MAPI  <br/> |
|Chamado pelo:  <br/> |Provedores de serviços  <br/> |
|Identificador de interface:  <br/> |IID_IMAPITableData  <br/> |
|Tipo de ponteiro:  <br/> |LPTABLEDATA  <br/> |
   
## <a name="vtable-order"></a>Ordem vtable

|||
|:-----|:-----|
|[HrGetView](itabledata-hrgetview.md) <br/> |Cria um modo de exibição de tabela, retornando um ponteiro para uma implementação [IMAPITable](imapitableiunknown.md) .  <br/> |
|[HrModifyRow](itabledata-hrmodifyrow.md) <br/> |Insere uma nova linha de tabela, possivelmente, substituindo uma linha existente.  <br/> |
|[HrDeleteRow](itabledata-hrdeleterow.md) <br/> |Exclui uma linha da tabela.  <br/> |
|[HrQueryRow](itabledata-hrqueryrow.md) <br/> |Recupera uma linha da tabela.  <br/> |
|[HrEnumRow](itabledata-hrenumrow.md) <br/> |Recupera uma linha com base em sua posição na tabela.  <br/> |
|[HrNotify](itabledata-hrnotify.md) <br/> |Envia uma notificação para uma linha da tabela.  <br/> |
|[HrInsertRow](itabledata-hrinsertrow.md) <br/> |Insere uma linha de tabela.  <br/> |
|[HrModifyRows](itabledata-hrmodifyrows.md) <br/> |Insere várias linhas de tabela, substituindo possivelmente linhas existentes.  <br/> |
|[HrDeleteRows](itabledata-hrdeleterows.md) <br/> |Exclui a várias linhas de tabela.  <br/> |
   
## <a name="remarks"></a>Comentários

A implementação de MAPI do **ITableData** funciona com tabelas, mantendo todos os dados e qualquer restrição associada na memória, tornando-o inadequados para uso com tabelas muito grandes. Restrições de grandes e operações complexas, como categorização não são suportadas. 
  
Objetos de dados de tabela identificam linhas usando uma coluna de índice, uma propriedade que é garantida que tenha um valor exclusivo para cada linha. A maioria dos provedores de serviço use a propriedade **PR_INSTANCE_KEY** ([PidTagInstanceKey](pidtaginstancekey-canonical-property.md)) como a coluna de índice. Propriedades com vários valores não podem ser usadas como uma coluna de índice.
  
Objetos de dados de tabela geram uma única notificação, independentemente do número de linhas afetadas por uma alteração ou exclusão. Se não existir uma linha de destino em uma operação, uma linha será adicionada.
  
## <a name="see-also"></a>Confira também



[Interfaces MAPI](mapi-interfaces.md)

