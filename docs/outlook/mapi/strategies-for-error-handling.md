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
  
Como os métodos de interface são virtuais, não é possível saber, como um chamador, o conjunto completo de valores que podem ser retornados de qualquer uma das chamadas. Uma implementação de um método pode retornar cinco valores; outra pode retornar oito. As entradas de referência na lista de documentação MAPI têm alguns valores que podem ser retornados para cada método; Estes são os valores que o cliente ou provedor de serviços pode verificar e lidar porque têm significados especiais. Outros valores podem ser retornados, mas por não serem significativos, não é necessário código especial para lidar com eles. Uma simples verificação de sucesso ou falha é adequada.
  
Alguns métodos de interface retornam avisos. Se um método que seu cliente ou provedor de serviços chamar puder retornar um aviso, use a macro **HR_FAILED** para testar o valor de retorno em vez de uma verificação de zero ou zero. Os avisos, embora não nulo, diferem dos códigos de erro, pois eles não têm o conjunto de bits alto. Se o cliente ou provedor de serviços não usar a macro, é provável que um aviso possa ser confundido para uma falha. 
  
Embora a maioria dos métodos e funções de interface retornem valores HRESULT, algumas funções retornam valores Long não assinados. Além disso, alguns métodos usados no ambiente MAPI são provenientes do COM e retornam valores de erro COM em vez de valores de erro MAPI. Tenha em mente as seguintes diretrizes ao fazer chamadas:
  
- Nunca confie ou use os valores de retorno de **IUnknown:: AddRef** ou **IUnknown:: Release**. Esses valores de retorno são apenas para fins de diagnóstico. 
    
- **IUnknown:: QueryInterface** sempre retorna erros com genéricos onde o recurso é FACILITY_NULL ou FACILITY_RPC, em vez de erros de MAPI. 
    
- Todos os outros métodos de interface retornam erros de interface MAPI com um recurso de erros do FACILITY_ITF ou do FACILITY_RPC ou do FACILITY_NULL.
    
Quando uma chamada é feita para um método MAPI sem suporte, um dos quatro possíveis erros pode ser retornado: 
  
MAPI_E_NO_SUPPORT
  
MAPI_E_INTERFACE_NOT_SUPPORTED
  
MAPI_E_INVALID_PARAMETER
  
MAPI_E_VERSION. 
  

