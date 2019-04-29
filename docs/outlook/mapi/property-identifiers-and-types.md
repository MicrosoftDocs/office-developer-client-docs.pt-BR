---
title: Identificadores e tipos de propriedade
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
# <a name="property-identifiers-and-types"></a>Identificadores e tipos de propriedade

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Todas as propriedades MAPI são representadas por marcas de propriedade. Uma marca de propriedade é um valor inteiro não assinado de 32 bits que contém o identificador da propriedade na alta ordem 16 bits e o tipo da propriedade na ordem baixa 16 bits. As marcas de propriedade para todas as propriedades definidas por MAPI estão incluídas no arquivo de cabeçalho Mapitags. h.
  
Os identificadores de propriedade são usados para indicar a que uma propriedade é usada e quem é responsável por ela. Os identificadores de propriedade são divididos por MAPI em intervalos; onde um identificador está no intervalo indica seu uso e propriedade. 
  
Os tipos de propriedade são usados para indicar o formato dos dados da propriedade. MAPI define todos os tipos válidos. Os clientes e provedores de serviços que criam novas propriedades devem usar um desses tipos. Todos os tipos de propriedade estão incluídos no arquivo de cabeçalho mapidefs. h.
  

