---
title: Tipos e identificadores de propriedade
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 39a5c97c-5ac8-47a8-b193-a4b3ba6a02a5
description: 'Última modificação: 23 de julho de 2011'
ms.openlocfilehash: caba60b7059d1c1f8f0440aeb55abb88801fbc9a
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33437214"
---
# <a name="property-identifiers-and-types"></a>Tipos e identificadores de propriedade

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Todas as propriedades MAPI são representadas por marcas de propriedade. A property tag is a 32-bit unsigned integer value that contains the property's identifier in the high order 16 bits and the property's type in the low order 16 bits. Marcas de propriedade para todas as propriedades definidas por MAPI estão incluídas no arquivo de título mapitags.h.
  
Identificadores de propriedade são usados para indicar para que uma propriedade é usada e para quem é responsável por ela. Os identificadores de propriedade são divididos por MAPI em intervalos; onde um identificador está no intervalo indica seu uso e propriedade. 
  
Tipos de propriedade são usados para indicar o formato dos dados da propriedade. MAPI define todos os tipos válidos. Clientes e provedores de serviços que criam novas propriedades devem usar um desses tipos. Todos os tipos de propriedade estão incluídos no arquivo de header mapidefs.h.
  

