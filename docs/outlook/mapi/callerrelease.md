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
description: '�ltima altera��o: segunda-feira, 9 de mar�o de 2015'
ms.openlocfilehash: 69ee06ef8c8f5499dec41232d3dc7b374b15a744
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19766239"
---
# <a name="callerrelease"></a>CALLERRELEASE

  
  
**Aplica-se a**: Outlook 
  
Define uma função de retorno de chamada que pode liberar um objeto de dados de tabela quando um modo de exibição de tabela está sendo lançado. 
  
|||
|:-----|:-----|
|Arquivo de cabeçalho:  <br/> |Mapiutil.h  <br/> |
|Função definido implementada por:  <br/> |Provedores de serviços e aplicativos cliente  <br/> |
|Função definido chamada pelo:  <br/> |MAPI  <br/> |
   
```cpp
void CALLERRELEASE(
  ULONG_PTR ulCallerData,
  LPTABLEDATA lpTblData,
  LPMAPITABLE lpVue
);
```

## <a name="parameters"></a>Par�metros

 _ulCallerData_
  
> [in] Dados do chamador salvo pelo MAPI com o modo de exibição de tabela e passado para o **CALLERRELEASE** com base em função de retorno de chamada. Os dados fornecem contexto sobre o modo de exibição de tabela que está sendo liberado. 
    
 _lpTblData_
  
> [in] Ponteiro para o [ITableData: IUnknown](itabledataiunknown.md) interface para o objeto de dados da tabela base na exibição da tabela que está sendo lançada. 
    
 _lpVue_
  
> [in] Ponteiro para o [IMAPITable: IUnknown](imapitableiunknown.md) interface para o modo de exibição de tabela que está sendo liberado. Esta é uma interface para o objeto table retornado no parâmetro _lppMAPITable_ do método [ITableData::HrGetView](itabledata-hrgetview.md) que criou o objeto ao lançamento. 
    
## <a name="return-value"></a>Valor retornado

None 
  
## <a name="remarks"></a>Comentários

Um aplicativo cliente ou um provedor de serviços que tenha preenchido um objeto de dados de tabela pode chamar [ITableData::HrGetView](itabledata-hrgetview.md) para criar um modo de exibição somente leitura, classificado da tabela. A chamada para **HrGetView** passa um ponteiro para uma função de retorno de chamada **CALLERRELEASE** com base e também um contexto a ser salvo com o modo de exibição de tabela. Quando a contagem de referência do modo de exibição tabela retorna como zero e o modo de exibição está sendo lançado, a implementação de **IMAPITable** chama a função de retorno de chamada, passando o contexto no parâmetro _ulCallerData_ . 
  
Um uso comum de uma função de retorno de chamada **CALLERRELEASE** com base é liberar o objeto de dados de tabela base e não precisará ficar atento aos-lo durante o processamento subsequente. 
  

