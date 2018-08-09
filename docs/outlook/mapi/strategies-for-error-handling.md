---
title: Estratégias para lidar com erros
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: be941efd-04b3-48d0-9b9c-8195ad2bb58d
description: '�ltima altera��o: s�bado, 23 de julho de 2011'
ms.openlocfilehash: e778df216d0fe9b901cd9f7136c8014a6b8f0d0a
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19770506"
---
# <a name="strategies-for-error-handling"></a>Estratégias para lidar com erros

  
  
**Aplica-se a**: Outlook 
  
Como os métodos de interface são virtuais, não é possível saber, como um chamador, o conjunto completo de valores que pode ser retornado de qualquer uma chamada. Uma implementação de um método pode retornar cinco valores; outro pode retornar oito. As entradas de referência na documentação de MAPI listam alguns valores que podem ser retornadas para cada método; Estes são os valores que seu provedor de cliente ou serviço pode procurar e manipular porque eles têm um significado especial. Outros valores podem ser retornados, mas porque eles não são significativos, código especial para lidar com aqueles não é necessário. Uma verificação simple para o sucesso ou falha é adequada.
  
Alguns métodos da interface retornam avisos. Se um método que chama o provedor de cliente ou serviço pode retornar um aviso, use a macro **HR_FAILED** para testar o valor de retorno em vez de uma verificação para zero ou diferente de zero. Avisos, embora diferente de zero, diferem dos códigos de erro em que não têm alto estará definido o bit definido. Se seu provedor de cliente ou serviço não usar a macro, é provável que um aviso pode ser errado para uma falha. 
  
Embora a maioria dos métodos de interface e funções retornam valores HRESULT, algumas funções retornam valores longos não assinados. Além disso, alguns métodos usados no ambiente de MAPI COM são provenientes e retornam valores de erro COM em vez de valores de erro MAPI. Tenha em mente as seguintes diretrizes ao fazer chamadas:
  
- Nunca dependa ou usar os valores de retorno de **AddRef** ou **IUnknown:: Release**. Esses valores de retorno são para fins de diagnóstico apenas. 
    
- **IUnknown:: QueryInterface** sempre retorna erros COM genéricos, onde o recurso é FACILITY_NULL ou FACILITY_RPC, em vez de erros MAPI. 
    
- Todos os outros métodos de interface retornam erros de interface MAPI com um recurso de FACILITY_ITF ou FACILITY_RPC ou FACILITY_NULL.
    
Quando uma chamada for feita para um método de MAPI sem suporte, uma das quatro possíveis erros pode ser retornada: 
  
MAPI_E_NO_SUPPORT
  
MAPI_E_INTERFACE_NOT_SUPPORTED
  
MAPI_E_INVALID_PARAMETER
  
MAPI_E_VERSION. 
  

