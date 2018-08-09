---
title: Transport Neutral Encapsulation Format (TNEF)
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 98d4fe3c-3908-4cd2-bfdb-ff1874a80b24
description: 'Última modificação: 12 de março de 2013'
ms.openlocfilehash: 34b64df25cb2f7f591f7c799dec957a0072840dc
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19770624"
---
# <a name="transport-neutral-encapsulation-format-tnef"></a><span data-ttu-id="3f0fa-103">Transport Neutral Encapsulation Format (TNEF)</span><span class="sxs-lookup"><span data-stu-id="3f0fa-103">Transport-Neutral Encapsulation Format (TNEF)</span></span>

 
  
<span data-ttu-id="3f0fa-104">**Aplica-se a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="3f0fa-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="3f0fa-105">TNEF é um formato para converter um conjunto de propriedades MAPI — uma mensagem MAPI — em um fluxo de dados serial.</span><span class="sxs-lookup"><span data-stu-id="3f0fa-105">TNEF is a format for converting a set of MAPI properties—a MAPI message—into a serial data stream.</span></span> <span data-ttu-id="3f0fa-106">As funções TNEF são usadas principalmente pelos provedores de transporte que precisa codificar propriedades de mensagem MAPI para transmissão através de um sistema de mensagens que não oferece suporte a essas propriedades diretamente.</span><span class="sxs-lookup"><span data-stu-id="3f0fa-106">The TNEF functions are primarily used by transport providers that need to encode MAPI message properties for transmission through a messaging system that does not support those properties directly.</span></span> <span data-ttu-id="3f0fa-107">Por exemplo, um transporte baseados em SMTP usa o TNEF para codificar propriedades como **PR_SENT_REPRESENTING_NAME** ([PidTagSentRepresentingName](pidtagsentrepresentingname-canonical-property.md)), que não possuem representações diretas na estrutura de uma mensagem de SMTP.</span><span class="sxs-lookup"><span data-stu-id="3f0fa-107">For example, an SMTP-based transport uses TNEF to encode properties like **PR_SENT_REPRESENTING_NAME** ([PidTagSentRepresentingName](pidtagsentrepresentingname-canonical-property.md)), which do not have direct representations in the structure of an SMTP message.</span></span>
  
<span data-ttu-id="3f0fa-108">A implementação de TNEF define vários atributos específicos TNEF, cada uma delas corresponde a uma determinada propriedade MAPI.</span><span class="sxs-lookup"><span data-stu-id="3f0fa-108">The TNEF implementation defines several TNEF-specific attributes, each of which corresponds to a particular MAPI property.</span></span> <span data-ttu-id="3f0fa-109">Esses atributos são usados para codificar suas respectivas propriedades MAPI no fluxo TNEF.</span><span class="sxs-lookup"><span data-stu-id="3f0fa-109">These attributes are used to encode their respective MAPI properties into the TNEF stream.</span></span> <span data-ttu-id="3f0fa-110">Além disso, um atributo especial é definido que pode ser usado para encapsular qualquer propriedade MAPI que não tem um atributo específico correspondente a ela.</span><span class="sxs-lookup"><span data-stu-id="3f0fa-110">In addition, a special attribute is defined that can be used to encapsulate any MAPI property that does not have a specific attribute corresponding to it.</span></span> <span data-ttu-id="3f0fa-111">O motivo pelo qual esses atributos forem definidos — em vez de simplesmente usar um método para todas as propriedades MAPI de codificação de uniforme — é permitir a compatibilidade com versões anteriores com o software não compatível com MAPI que está usando o TNEF.</span><span class="sxs-lookup"><span data-stu-id="3f0fa-111">The reason these attributes are defined — instead of simply using a uniform encoding method for all MAPI properties — is to enable backward compatibility with non-MAPI-compliant software that is using TNEF.</span></span>
  
<span data-ttu-id="3f0fa-112">O restante desta seção descreve a estrutura e a sintaxe de um stream TNEF, o mapeamento entre propriedades MAPI e atributos TNEF e considerações importantes sobre determinados atributos TNEF.</span><span class="sxs-lookup"><span data-stu-id="3f0fa-112">The remainder of this section describes the structure and syntax of a TNEF stream, the mapping between MAPI properties and TNEF attributes, and important considerations for certain TNEF attributes.</span></span>
  

