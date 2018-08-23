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
ms.openlocfilehash: c165bcaedfc3dbab0c950d0674228b15dfeee958
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22592273"
---
# <a name="hrqueryallrows"></a>HrQueryAllRows

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Recupera todas as linhas de uma tabela. 
  
|||
|:-----|:-----|
|Arquivo de cabeçalho:  <br/> |Mapiutil.h  <br/> |
|Implementada por:  <br/> |MAPI  <br/> |
|Chamado pelo:  <br/> |Provedores de serviços e aplicativos cliente  <br/> |
   
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
  
> [in] Ponteiro para a tabela MAPI do qual as linhas são recuperadas. 
    
 _ptaga_
  
> [in] Ponteiro para uma estrutura [SPropTagArray](sproptagarray.md) que contém uma matriz de propriedade marcas indicando colunas da tabela. Essas marcas são usadas para selecionar as colunas específicas a serem recuperadas. Se o parâmetro _ptaga_ for NULL, **HrQueryAllRows** recupera o conjunto de coluna inteira do modo de exibição de tabela atual passado no parâmetro _ptable_ . 
    
 _pré-instalação_
  
> [in] Ponteiro para uma estrutura [SRestriction](srestriction.md) que contém as restrições de recuperação. Se o parâmetro de _pré-instalação_ for NULL, **HrQueryAllRows** torna sem restrições. 
    
 _PSOs_
  
> [in] Ponteiro para uma estrutura [SSortOrderSet](ssortorderset.md) que identifica a ordem de classificação das colunas a serem recuperadas. Se o parâmetro _psos_ for NULL, a ordem de classificação padrão para a tabela será usada. 
    
 _crowsMax_
  
> [in] Número máximo de linhas a serem recuperadas. Se o valor do parâmetro _crowsMax_ for zero, nenhum limite no número de linhas recuperadas é definido. 
    
 _pprows_
  
> [out] Ponteiro para um ponteiro para a estrutura [SRowSet](srowset.md) retornado que contém uma matriz de ponteiros para as linhas de tabela recuperadas. 
    
## <a name="return-value"></a>Valor retornado

S_OK 
  
> A chamada recuperado as linhas esperadas de uma tabela. 
    
MAPI_E_TABLE_TOO_BIG 
  
> O número de linhas da tabela é maior que o número passado para o parâmetro _crowsMax_ . 
    
## <a name="remarks"></a>Comentários

Um aplicativo cliente ou um provedor de serviços não tem controle sobre o número de linhas **que HrQueryAllRows** tenta recuperar, diferente de, impondo uma restrição apontado pelo parâmetro _pré-instalação_ . O parâmetro _crowsMax_ não limitam a recuperação para um determinado número de linhas da tabela, mas em vez disso, define uma quantidade máxima de memória disponível para abrigar recuperadas todas as linhas. A única proteção contra estouro de memória enorme é o recurso de provisórias fornecido, definindo _crowsMax_. O retorno de erro MAPI_E_TABLE_TOO_BIG significa que a tabela contém muitas linhas seja mantido todo ao mesmo tempo na memória. 
  
Tabelas que são normalmente pequenas, como uma tabela de repositório de mensagens ou de uma tabela de provedor, geralmente podem ser com segurança recuperadas com **HrQueryAllRows**. Tabelas em risco de ser muito grande, como uma tabela de conteúdo ou até mesmo uma tabela de destinatários, devem ser percorridas nas subseções usando o método [IMAPITable:: QueryRows](imapitable-queryrows.md) . 
  
Se houver qualquer tabela propriedades indefinidas quando **HrQueryAllRows** é chamado, são retornadas com o tipo de propriedade PT_NULL e o identificador de propriedade PROP_ID_NULL 
  

