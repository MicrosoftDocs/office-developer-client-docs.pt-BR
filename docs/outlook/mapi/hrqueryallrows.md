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
|Arquivo de cabeçalho:  <br/> |Mapiutil. h  <br/> |
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

 _PTable_
  
> no Ponteiro para a tabela MAPI da qual as linhas são recuperadas. 
    
 _ptaga_
  
> no Ponteiro para uma estrutura [SPropTagArray](sproptagarray.md) que contém uma matriz de marcas de propriedade que indicam as colunas da tabela. Essas marcas são usadas para selecionar as colunas específicas a serem recuperadas. Se o parâmetro _ptaga_ for NULL, **HrQueryAllRows** recuperará todo o conjunto de colunas do modo de exibição de tabela atual passado no parâmetro _PTable_ . 
    
 _pré-instalação_
  
> no Ponteiro para uma estrutura [SRestriction](srestriction.md) que contém restrições de recuperação. Se o parâmetro _Pres_ for NULL, **HrQueryAllRows** não fará nenhuma restrição. 
    
 _PSOs_
  
> no Ponteiro para uma estrutura [SSortOrderSet](ssortorderset.md) identificando a ordem de classificação das colunas a serem recuperadas. Se o parâmetro _PSOs_ for NULL, a ordem de classificação padrão para a tabela será usada. 
    
 _crowsMax_
  
> no Número máximo de linhas a serem recuperadas. Se o valor do parâmetro _crowsMax_ for zero, nenhum limite no número de linhas recuperadas será definido. 
    
 _pprows_
  
> bota Ponteiro para um ponteiro para a estrutura [SRowSet](srowset.md) retornada que contém uma matriz de ponteiros para as linhas da tabela recuperadas. 
    
## <a name="return-value"></a>Valor de retorno

S_OK 
  
> A chamada recuperou as linhas esperadas de uma tabela. 
    
MAPI_E_TABLE_TOO_BIG 
  
> O número de linhas na tabela é maior do que o número passado para o parâmetro _crowsMax_ . 
    
## <a name="remarks"></a>Comentários

Um aplicativo cliente ou provedor de serviços não tem controle sobre o número de linhas que o **HrQueryAllRows** tenta recuperar, exceto por impor uma restrição apontada pelo parâmetro _Pres_ . O parâmetro _crowsMax_ não limita a recuperação a um determinado número de linhas de tabela, mas, em vez disso, define uma quantidade máxima de memória disponível para armazenar todas as linhas recuperadas. A única proteção contra estouro de memória maciça é o recurso stopgap fornecido pela configuração _crowsMax_. O erro de retorno MAPI_E_TABLE_TOO_BIG significa que a tabela contém muitas linhas a serem mantidas de uma só vez na memória. 
  
As tabelas que são normalmente pequenas, como uma tabela de repositório de mensagens ou uma tabela de provedor, geralmente podem ser recuperadas com segurança com o **HrQueryAllRows**. As tabelas em risco de ser muito grande, como uma tabela de conteúdo ou mesmo uma tabela de destinatários, devem ser percorridas em subseções usando o método imApitable [:: QueryRows](imapitable-queryrows.md) . 
  
Se qualquer propriedade da tabela estiver indefinida quando **HrQueryAllRows** for chamado, elas serão retornadas com o tipo de propriedade PT_NULL e o identificador de propriedade PROP_ID_NULL 
  

