---
title: Estratégias para tratamento de erros
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: be941efd-04b3-48d0-9b9c-8195ad2bb58d
description: 'Última modificação: 23 de julho de 2011'
ms.openlocfilehash: 9e76ae3f292d8348b9dc64cb54bffae96b96e871
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33424144"
---
# <a name="strategies-for-error-handling"></a>Estratégias para tratamento de erros

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Como os métodos de interface são virtuais, não é possível saber, como chamador, o conjunto completo de valores que podem ser retornados de qualquer chamada. Uma implementação de um método pode retornar cinco valores; outro pode retornar oito. As entradas de referência na lista de documentação MAPI listam alguns valores que podem ser retornados para cada método; esses são os valores que seu cliente ou provedor de serviços pode verificar e manipular porque eles têm significados especiais. Outros valores podem ser retornados, mas como não são significativos, o código especial para lidar com eles não é necessário. Uma verificação simples de sucesso ou falha é adequada.
  
Alguns métodos de interface retornam avisos. Se um método que seu cliente ou provedor de serviços chama puder retornar um aviso, use a macro **HR_FAILED** para testar o valor de retorno em vez de uma verificação de zero ou diferente de zero. Avisos, embora diferentes de zero, diferem dos códigos de erro porque eles não têm o bit alto definido. Se o seu cliente ou provedor de serviços não usar a macro, é provável que um aviso possa ser confundido por uma falha. 
  
Embora a maioria dos métodos e funções de interface retorne valores HRESULT, algumas funções retornam valores longos não assinados. Além disso, alguns métodos usados no ambiente MAPI vêm de COM e retornam valores de erro COM em vez de valores de erro MAPI. Lembre-se das seguintes diretrizes ao fazer chamadas:
  
- Nunca confie ou use os valores de retorno de **IUnknown::AddRef** ou **IUnknown::Release**. Esses valores de retorno são apenas para fins de diagnóstico. 
    
- **IUnknown::QueryInterface** sempre retorna erros DE COM genéricos em que o recurso é FACILITY_NULL ou FACILITY_RPC, em vez de erros MAPI. 
    
- Todos os outros métodos de interface retornam erros de interface MAPI com um recurso de FACILITY_ITF, FACILITY_RPC ou FACILITY_NULL erros.
    
Quando uma chamada é feita para um método MAPI sem suporte, um dos quatro erros possíveis pode ser retornado: 
  
MAPI_E_NO_SUPPORT
  
MAPI_E_INTERFACE_NOT_SUPPORTED
  
MAPI_E_INVALID_PARAMETER
  
MAPI_E_VERSION. 
  

