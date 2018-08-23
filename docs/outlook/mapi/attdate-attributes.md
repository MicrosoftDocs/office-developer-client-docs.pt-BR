---
title: Atributos attDate
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 22801641-752c-4c81-be90-02039eaa4277
description: '�ltima altera��o: s�bado, 23 de julho de 2011'
ms.openlocfilehash: ff0cc6b1c17b2ed83d7b0ec0921904763da8624b
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22567010"
---
# <a name="attdate-attributes"></a><span data-ttu-id="8e90e-103">Atributos attDate</span><span class="sxs-lookup"><span data-stu-id="8e90e-103">attDate Attributes</span></span>

  
  
<span data-ttu-id="8e90e-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="8e90e-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="8e90e-105">Todas as propriedades MAPI relativos ao datas e horas são mapeadas para os atributos TNEF que possuem o prefixo **attDate** .</span><span class="sxs-lookup"><span data-stu-id="8e90e-105">All MAPI properties relating to dates and times are mapped to TNEF attributes that have the **attDate** prefix.</span></span> <span data-ttu-id="8e90e-106">Estas são codificadas como estruturas **DTR** .</span><span class="sxs-lookup"><span data-stu-id="8e90e-106">These are all encoded as **DTR** structures.</span></span> <span data-ttu-id="8e90e-107">As datas e horas dos atributos do anexo são codificadas como **DTR** estruturas também.</span><span class="sxs-lookup"><span data-stu-id="8e90e-107">The dates and times for attachment attributes are encoded as **DTR** structures as well.</span></span> 
  
<span data-ttu-id="8e90e-108">Todas as propriedades MAPI relativos ao datas e horas são mapeadas para os atributos TNEF que possuem o prefixo **attDate** .</span><span class="sxs-lookup"><span data-stu-id="8e90e-108">All MAPI properties relating to dates and times are mapped to TNEF attributes that have the **attDate** prefix.</span></span> <span data-ttu-id="8e90e-109">Estas são codificadas como estruturas **DTR** .</span><span class="sxs-lookup"><span data-stu-id="8e90e-109">These are all encoded as **DTR** structures.</span></span> <span data-ttu-id="8e90e-110">As datas e horas dos atributos do anexo são codificadas como **DTR** estruturas também.</span><span class="sxs-lookup"><span data-stu-id="8e90e-110">The dates and times for attachment attributes are encoded as **DTR** structures as well.</span></span> 
  
<span data-ttu-id="8e90e-111">Uma estrutura **DTR** é muito semelhante à estrutura **SYSTEMTIME** definida nos arquivos de cabeçalho Win32.</span><span class="sxs-lookup"><span data-stu-id="8e90e-111">A **DTR** structure is very similar to the **SYSTEMTIME** structure defined in the Win32 header files.</span></span> <span data-ttu-id="8e90e-112">A estrutura **DTR** é codificada no stream TNEF como bytes **sizeof(DTR)** começando com o primeiro membro da estrutura.</span><span class="sxs-lookup"><span data-stu-id="8e90e-112">The **DTR** structure is encoded in the TNEF stream as **sizeof(DTR)** bytes starting with the first member of the structure.</span></span> <span data-ttu-id="8e90e-113">A estrutura **DTR** é definida no TNEF. Arquivo de cabeçalho H.</span><span class="sxs-lookup"><span data-stu-id="8e90e-113">The **DTR** structure is defined in the TNEF.H header file.</span></span> 
  

