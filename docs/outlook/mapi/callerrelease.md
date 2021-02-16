---
title: CALLERRELEASE
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- CALLERRELEASE
api_type:
- HeaderDef
ms.assetid: 80ba893d-3380-4db1-9175-f5b84cb57def
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: 9a22550e60c9de38236a9f612c7e60f50f18978f
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33408723"
---
# <a name="callerrelease"></a>CALLERRELEASE

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Define uma função de retorno de chamada que pode liberar um objeto de dados de tabela quando um exibição de tabela está sendo liberado. 
  
|||
|:-----|:-----|
|Arquivo de cabeçalho:  <br/> |Mapiutil.h  <br/> |
|Função definida implementada por:  <br/> |Aplicativos cliente e provedores de serviços  <br/> |
|Função definida chamada por:  <br/> |MAPI  <br/> |
   
```cpp
void CALLERRELEASE(
  ULONG_PTR ulCallerData,
  LPTABLEDATA lpTblData,
  LPMAPITABLE lpVue
);
```

## <a name="parameters"></a>Parâmetros

 _ulCallerData_
  
> [in] Dados do chamador salvos por MAPI com o exibição de tabela e passados para a função de retorno de chamada baseada em **CALLERRELEASE.** Os dados proporcionam contexto sobre a exibição de tabela que está sendo liberada. 
    
 _lpTblData_
  
> [in] Ponteiro para a [interface ITableData : IUnknown](itabledataiunknown.md) para o objeto de dados de tabela subjacente à exibição de tabela que está sendo liberada. 
    
 _lpVue_
  
> [in] Ponteiro para a [interface IMAPITable : IUnknown](imapitableiunknown.md) para o exibição de tabela que está sendo liberado. Esta é uma interface para o objeto table retornado no parâmetro  _lppMAPITable_ do método [ITableData::HrGetView](itabledata-hrgetview.md) que criou o objeto a ser liberado. 
    
## <a name="return-value"></a>Valor de retorno

Nenhum 
  
## <a name="remarks"></a>Comentários

Um aplicativo cliente ou provedor de serviços que preencheu um objeto de dados de tabela pode chamar [ITableData::HrGetView](itabledata-hrgetview.md) para criar uma exibição de somente leitura e classificação da tabela. A chamada para **HrGetView** passa um ponteiro para uma função de retorno de chamada baseada em **CALLERRELEASE** e também um contexto a ser salvo com o exibição de tabela. Quando a contagem de referência do exibição de tabela retorna para zero e o exibição está sendo liberado, a implementação **IMAPITable** chama a função de retorno de chamada, passando o contexto no _parâmetro ulCallerData._ 
  
Um uso comum de uma função de retorno de chamada baseada em **CALLERRELEASE** é liberar o objeto de dados da tabela subjacente e não precisa rastreá-lo durante o processamento subsequente. 
  

