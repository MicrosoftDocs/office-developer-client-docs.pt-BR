---
title: HrQueryAllRows
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- HrQueryAllRows
api_type:
- HeaderDef
ms.assetid: b08fadcf-cdf3-48b7-9489-d7f745266482
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: 0f09304f21180d9ebc2a1e1dcc54ebadd3622804
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33422891"
---
# <a name="hrqueryallrows"></a>HrQueryAllRows

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Recupera todas as linhas de uma tabela. 
  
|||
|:-----|:-----|
|Arquivo de cabeçalho:  <br/> |Mapiutil.h  <br/> |
|Implementado por:  <br/> |MAPI  <br/> |
|Chamado por:  <br/> |Aplicativos cliente e provedores de serviços  <br/> |
   
```cpp
HRESULT HrQueryAllRows(
  LPMAPITABLE ptable,
  LPSPropTagArray ptaga,
  LPSRestriction pres,
  LPSSortOrderSet psos,
  LONG crowsMax,
  LPSRowSet FAR * pprows
);
```

## <a name="parameters"></a>Parâmetros

 _ptable_
  
> [in] Ponteiro para a tabela MAPI da qual as linhas são recuperadas. 
    
 _ptaga_
  
> [in] Ponteiro para uma [estrutura SPropTagArray](sproptagarray.md) que contém uma matriz de marcas de propriedade que indicam colunas de tabela. Essas marcas são usadas para selecionar as colunas específicas a serem recuperadas. Se o _parâmetro ptaga_ for NULL, **HrQueryAllRows** recuperará todo o conjunto de colunas do atual exibição de tabela passado no parâmetro _ptable._ 
    
 _pres_
  
> [in] Ponteiro para uma [estrutura SRestriction](srestriction.md) que contém restrições de recuperação. Se o  _parâmetro pré-definido_ for NULL, **HrQueryAllRows** não fará restrições. 
    
 _psos_
  
> [in] Ponteiro para uma [estrutura SSortOrderSet](ssortorderset.md) que identifica a ordem de classificação das colunas a serem recuperadas. Se o  _parâmetro psos_ for NULL, a ordem de classificação padrão para a tabela será usada. 
    
 _aaa._
  
> [in] Número máximo de linhas a serem recuperadas. Se o valor do  _parâmetromax for_ zero, nenhum limite no número de linhas recuperadas será definido. 
    
 _pprows_
  
> [out] Ponteiro para um ponteiro para a estrutura [SRowSet](srowset.md) retornada que contém uma matriz de ponteiros para as linhas recuperadas da tabela. 
    
## <a name="return-value"></a>Valor de retorno

S_OK 
  
> A chamada recuperou as linhas esperadas de uma tabela. 
    
MAPI_E_TABLE_TOO_BIG 
  
> O número de linhas na tabela é maior que o número passado para o _parâmetromax._ 
    
## <a name="remarks"></a>Comentários

Um aplicativo cliente ou provedor de serviços não tem controle sobre o número de linhas **que HrQueryAllRows** tenta recuperar, além de impor uma restrição apontada pelo parâmetro _pré-definido._ O  _parâmetromax não_ limita a recuperação a um determinado número de linhas de tabela, mas define uma quantidade máxima de memória disponível para manter todas as linhas recuperadas. A única proteção contra estouro de memória grande é o recurso stopgap fornecido pela configuração  _demax_. O erro retorna MAPI_E_TABLE_TOO_BIG significa que a tabela contém linhas demais para serem mantidas todas de uma vez na memória. 
  
Tabelas que normalmente são pequenas, como uma tabela de armazenamento de mensagens ou uma tabela de provedor, geralmente podem ser recuperadas com segurança com **HrQueryAllRows**. Tabelas com risco de serem muito grandes, como uma tabela de conteúdo ou até mesmo uma tabela de destinatários, devem ser percorridas em subseções usando o método [IMAPITable::QueryRows.](imapitable-queryrows.md) 
  
Se alguma propriedade de tabela for indefinida quando **HrQueryAllRows** for chamado, elas serão retornadas com o tipo de propriedade PT_NULL e o identificador de PROP_ID_NULL 
  

