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
# <a name="property-identifiers-and-types"></a><span data-ttu-id="60f86-103">Tipos e identificadores de propriedade</span><span class="sxs-lookup"><span data-stu-id="60f86-103">Property Identifiers and Types</span></span>

  
  
<span data-ttu-id="60f86-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="60f86-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="60f86-105">Todas as propriedades MAPI são representadas por marcas de propriedade.</span><span class="sxs-lookup"><span data-stu-id="60f86-105">All MAPI properties are represented by property tags.</span></span> <span data-ttu-id="60f86-106">A property tag is a 32-bit unsigned integer value that contains the property's identifier in the high order 16 bits and the property's type in the low order 16 bits.</span><span class="sxs-lookup"><span data-stu-id="60f86-106">A property tag is a 32-bit unsigned integer value that contains the property's identifier in the high order 16 bits and the property's type in the low order 16 bits.</span></span> <span data-ttu-id="60f86-107">Marcas de propriedade para todas as propriedades definidas por MAPI estão incluídas no arquivo de título mapitags.h.</span><span class="sxs-lookup"><span data-stu-id="60f86-107">Property tags for all of the properties defined by MAPI are included in the mapitags.h header file.</span></span>
  
<span data-ttu-id="60f86-108">Identificadores de propriedade são usados para indicar para que uma propriedade é usada e para quem é responsável por ela.</span><span class="sxs-lookup"><span data-stu-id="60f86-108">Property identifiers are used to indicate what a property is used for and who is responsible for it.</span></span> <span data-ttu-id="60f86-109">Os identificadores de propriedade são divididos por MAPI em intervalos; onde um identificador está no intervalo indica seu uso e propriedade.</span><span class="sxs-lookup"><span data-stu-id="60f86-109">Property identifiers are divided by MAPI into ranges; where an identifier falls in the range indicates its use and ownership.</span></span> 
  
<span data-ttu-id="60f86-110">Tipos de propriedade são usados para indicar o formato dos dados da propriedade.</span><span class="sxs-lookup"><span data-stu-id="60f86-110">Property types are used to indicate the format of the property's data.</span></span> <span data-ttu-id="60f86-111">MAPI define todos os tipos válidos.</span><span class="sxs-lookup"><span data-stu-id="60f86-111">MAPI defines all of the valid types.</span></span> <span data-ttu-id="60f86-112">Clientes e provedores de serviços que criam novas propriedades devem usar um desses tipos.</span><span class="sxs-lookup"><span data-stu-id="60f86-112">Clients and service providers creating new properties must use one of these types.</span></span> <span data-ttu-id="60f86-113">Todos os tipos de propriedade estão incluídos no arquivo de header mapidefs.h.</span><span class="sxs-lookup"><span data-stu-id="60f86-113">All of the property types are included in the mapidefs.h header file.</span></span>
  

