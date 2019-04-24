---
title: Atributos attDate
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 22801641-752c-4c81-be90-02039eaa4277
description: 'Última modificação: 23 de julho de 2011'
ms.openlocfilehash: b7c1ce8d0338a2bda63a276628bdd6e8be3b8eb1
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32318064"
---
# <a name="attdate-attributes"></a><span data-ttu-id="9782e-103">Atributos attDate</span><span class="sxs-lookup"><span data-stu-id="9782e-103">attDate Attributes</span></span>

  
  
<span data-ttu-id="9782e-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="9782e-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="9782e-105">Todas as propriedades MAPI relacionadas a datas e horas são mapeadas para atributos TNEF que têm o prefixo **attDate** .</span><span class="sxs-lookup"><span data-stu-id="9782e-105">All MAPI properties relating to dates and times are mapped to TNEF attributes that have the **attDate** prefix.</span></span> <span data-ttu-id="9782e-106">Todos são codificados como estruturas de **DTR** .</span><span class="sxs-lookup"><span data-stu-id="9782e-106">These are all encoded as **DTR** structures.</span></span> <span data-ttu-id="9782e-107">As datas e horas para atributos de anexo também são codificadas como estruturas de **DTR** .</span><span class="sxs-lookup"><span data-stu-id="9782e-107">The dates and times for attachment attributes are encoded as **DTR** structures as well.</span></span> 
  
<span data-ttu-id="9782e-108">Todas as propriedades MAPI relacionadas a datas e horas são mapeadas para atributos TNEF que têm o prefixo **attDate** .</span><span class="sxs-lookup"><span data-stu-id="9782e-108">All MAPI properties relating to dates and times are mapped to TNEF attributes that have the **attDate** prefix.</span></span> <span data-ttu-id="9782e-109">Todos são codificados como estruturas de **DTR** .</span><span class="sxs-lookup"><span data-stu-id="9782e-109">These are all encoded as **DTR** structures.</span></span> <span data-ttu-id="9782e-110">As datas e horas para atributos de anexo também são codificadas como estruturas de **DTR** .</span><span class="sxs-lookup"><span data-stu-id="9782e-110">The dates and times for attachment attributes are encoded as **DTR** structures as well.</span></span> 
  
<span data-ttu-id="9782e-111">Uma estrutura **DTR** é muito parecida com a estrutura **SYSTEMTIME** definida nos arquivos de cabeçalho do Win32.</span><span class="sxs-lookup"><span data-stu-id="9782e-111">A **DTR** structure is very similar to the **SYSTEMTIME** structure defined in the Win32 header files.</span></span> <span data-ttu-id="9782e-112">A estrutura **DTR** é codificada nos bytes de fluxo TNEF como **sizeof (DTR)** começando com o primeiro membro da estrutura.</span><span class="sxs-lookup"><span data-stu-id="9782e-112">The **DTR** structure is encoded in the TNEF stream as **sizeof(DTR)** bytes starting with the first member of the structure.</span></span> <span data-ttu-id="9782e-113">A estrutura **DTR** é definida no TNEF. Arquivo de cabeçalho H.</span><span class="sxs-lookup"><span data-stu-id="9782e-113">The **DTR** structure is defined in the TNEF.H header file.</span></span> 
  

