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
ms.openlocfilehash: f3319c9ae49fa97a6179b0ee800bd5dd594aefab
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19766202"
---
# <a name="attdate-attributes"></a><span data-ttu-id="a902c-103">Atributos attDate</span><span class="sxs-lookup"><span data-stu-id="a902c-103">attDate Attributes</span></span>

  
  
<span data-ttu-id="a902c-104">**Aplica-se a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="a902c-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="a902c-105">Todas as propriedades MAPI relativos ao datas e horas são mapeadas para os atributos TNEF que possuem o prefixo **attDate** .</span><span class="sxs-lookup"><span data-stu-id="a902c-105">All MAPI properties relating to dates and times are mapped to TNEF attributes that have the **attDate** prefix.</span></span> <span data-ttu-id="a902c-106">Estas são codificadas como estruturas **DTR** .</span><span class="sxs-lookup"><span data-stu-id="a902c-106">These are all encoded as **DTR** structures.</span></span> <span data-ttu-id="a902c-107">As datas e horas dos atributos do anexo são codificadas como **DTR** estruturas também.</span><span class="sxs-lookup"><span data-stu-id="a902c-107">The dates and times for attachment attributes are encoded as **DTR** structures as well.</span></span> 
  
<span data-ttu-id="a902c-108">Todas as propriedades MAPI relativos ao datas e horas são mapeadas para os atributos TNEF que possuem o prefixo **attDate** .</span><span class="sxs-lookup"><span data-stu-id="a902c-108">All MAPI properties relating to dates and times are mapped to TNEF attributes that have the **attDate** prefix.</span></span> <span data-ttu-id="a902c-109">Estas são codificadas como estruturas **DTR** .</span><span class="sxs-lookup"><span data-stu-id="a902c-109">These are all encoded as **DTR** structures.</span></span> <span data-ttu-id="a902c-110">As datas e horas dos atributos do anexo são codificadas como **DTR** estruturas também.</span><span class="sxs-lookup"><span data-stu-id="a902c-110">The dates and times for attachment attributes are encoded as **DTR** structures as well.</span></span> 
  
<span data-ttu-id="a902c-111">Uma estrutura **DTR** é muito semelhante à estrutura **SYSTEMTIME** definida nos arquivos de cabeçalho Win32.</span><span class="sxs-lookup"><span data-stu-id="a902c-111">A **DTR** structure is very similar to the **SYSTEMTIME** structure defined in the Win32 header files.</span></span> <span data-ttu-id="a902c-112">A estrutura **DTR** é codificada no stream TNEF como bytes **sizeof(DTR)** começando com o primeiro membro da estrutura.</span><span class="sxs-lookup"><span data-stu-id="a902c-112">The **DTR** structure is encoded in the TNEF stream as **sizeof(DTR)** bytes starting with the first member of the structure.</span></span> <span data-ttu-id="a902c-113">A estrutura **DTR** é definida no TNEF. Arquivo de cabeçalho H.</span><span class="sxs-lookup"><span data-stu-id="a902c-113">The **DTR** structure is defined in the TNEF.H header file.</span></span> 
  

