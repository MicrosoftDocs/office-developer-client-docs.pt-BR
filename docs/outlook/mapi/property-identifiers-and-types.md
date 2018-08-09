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
ms.openlocfilehash: 7f31162e669af6efaf9e935c7c400d105c1321c2
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19770183"
---
# <a name="property-identifiers-and-types"></a><span data-ttu-id="6b566-103">Tipos e identificadores de propriedades</span><span class="sxs-lookup"><span data-stu-id="6b566-103">Property Identifiers and Types</span></span>

  
  
<span data-ttu-id="6b566-104">**Aplica-se a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="6b566-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="6b566-105">Todas as propriedades MAPI são representadas por marcas de propriedade.</span><span class="sxs-lookup"><span data-stu-id="6b566-105">All MAPI properties are represented by property tags.</span></span> <span data-ttu-id="6b566-106">Uma marca de propriedade é um valor inteiro não assinado de 32 bits que contém o identificador da propriedade na alta pedidos de 16 bits e o tipo da propriedade no fraca pedidos de 16 bits.</span><span class="sxs-lookup"><span data-stu-id="6b566-106">A property tag is a 32-bit unsigned integer value that contains the property's identifier in the high order 16 bits and the property's type in the low order 16 bits.</span></span> <span data-ttu-id="6b566-107">Marcas de propriedade para todas as propriedades definidas pelo MAPI são incluídas no arquivo de cabeçalho mapitags.h.</span><span class="sxs-lookup"><span data-stu-id="6b566-107">Property tags for all of the properties defined by MAPI are included in the mapitags.h header file.</span></span>
  
<span data-ttu-id="6b566-108">Identificadores de propriedade são usados para indicar que uma propriedade é usada e quem é responsável por ela.</span><span class="sxs-lookup"><span data-stu-id="6b566-108">Property identifiers are used to indicate what a property is used for and who is responsible for it.</span></span> <span data-ttu-id="6b566-109">Identificadores de propriedade são divididos por MAPI em intervalos; onde um identificador cai no intervalo indica seu uso e a propriedade.</span><span class="sxs-lookup"><span data-stu-id="6b566-109">Property identifiers are divided by MAPI into ranges; where an identifier falls in the range indicates its use and ownership.</span></span> 
  
<span data-ttu-id="6b566-110">Tipos de propriedade são usados para indicar o formato dos dados da propriedade.</span><span class="sxs-lookup"><span data-stu-id="6b566-110">Property types are used to indicate the format of the property's data.</span></span> <span data-ttu-id="6b566-111">MAPI define todos os tipos válidos.</span><span class="sxs-lookup"><span data-stu-id="6b566-111">MAPI defines all of the valid types.</span></span> <span data-ttu-id="6b566-112">Clientes e provedores de serviço de criação de novas propriedades devem usar um desses tipos.</span><span class="sxs-lookup"><span data-stu-id="6b566-112">Clients and service providers creating new properties must use one of these types.</span></span> <span data-ttu-id="6b566-113">Todos os tipos de propriedade são incluídos no arquivo de cabeçalho mapidefs.h.</span><span class="sxs-lookup"><span data-stu-id="6b566-113">All of the property types are included in the mapidefs.h header file.</span></span>
  

