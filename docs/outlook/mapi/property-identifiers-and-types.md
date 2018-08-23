---
title: Tipos e identificadores de propriedades
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 39a5c97c-5ac8-47a8-b193-a4b3ba6a02a5
description: '�ltima altera��o: s�bado, 23 de julho de 2011'
ms.openlocfilehash: 423992e0485e8e3092cfc4126164576906d51149
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22567059"
---
# <a name="property-identifiers-and-types"></a>Tipos e identificadores de propriedades

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Todas as propriedades MAPI são representadas por marcas de propriedade. Uma marca de propriedade é um valor inteiro não assinado de 32 bits que contém o identificador da propriedade na alta pedidos de 16 bits e o tipo da propriedade no fraca pedidos de 16 bits. Marcas de propriedade para todas as propriedades definidas pelo MAPI são incluídas no arquivo de cabeçalho mapitags.h.
  
Identificadores de propriedade são usados para indicar que uma propriedade é usada e quem é responsável por ela. Identificadores de propriedade são divididos por MAPI em intervalos; onde um identificador cai no intervalo indica seu uso e a propriedade. 
  
Tipos de propriedade são usados para indicar o formato dos dados da propriedade. MAPI define todos os tipos válidos. Clientes e provedores de serviço de criação de novas propriedades devem usar um desses tipos. Todos os tipos de propriedade são incluídos no arquivo de cabeçalho mapidefs.h.
  

