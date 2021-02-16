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
ms.openlocfilehash: d902039fa1081e30947ddd8f70ead9ae7acec06a
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33428687"
---
# <a name="transport-neutral-encapsulation-format-tnef"></a><span data-ttu-id="07f27-103">Transport Neutral Encapsulation Format (TNEF)</span><span class="sxs-lookup"><span data-stu-id="07f27-103">Transport-Neutral Encapsulation Format (TNEF)</span></span>

 
  
<span data-ttu-id="07f27-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="07f27-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="07f27-105">O TNEF é um formato para converter um conjunto de propriedades MAPI — uma mensagem MAPI — em um fluxo serial de dados.</span><span class="sxs-lookup"><span data-stu-id="07f27-105">TNEF is a format for converting a set of MAPI properties—a MAPI message—into a serial data stream.</span></span> <span data-ttu-id="07f27-106">As funções TNEF são usadas principalmente por provedores de transporte que precisam codificar propriedades de mensagens MAPI para transmissão por meio de um sistema de mensagens que não suporta essas propriedades diretamente.</span><span class="sxs-lookup"><span data-stu-id="07f27-106">The TNEF functions are primarily used by transport providers that need to encode MAPI message properties for transmission through a messaging system that does not support those properties directly.</span></span> <span data-ttu-id="07f27-107">Por exemplo, um transporte baseado em SMTP usa TNEF para codificar propriedades como **PR_SENT_REPRESENTING_NAME** ([PidTagSentRepresentingName](pidtagsentrepresentingname-canonical-property.md)), que não têm representações diretas na estrutura de uma mensagem SMTP.</span><span class="sxs-lookup"><span data-stu-id="07f27-107">For example, an SMTP-based transport uses TNEF to encode properties like **PR_SENT_REPRESENTING_NAME** ([PidTagSentRepresentingName](pidtagsentrepresentingname-canonical-property.md)), which do not have direct representations in the structure of an SMTP message.</span></span>
  
<span data-ttu-id="07f27-108">A implementação do TNEF define vários atributos específicos do TNEF, cada um deles corresponde a uma propriedade MAPI específica.</span><span class="sxs-lookup"><span data-stu-id="07f27-108">The TNEF implementation defines several TNEF-specific attributes, each of which corresponds to a particular MAPI property.</span></span> <span data-ttu-id="07f27-109">Esses atributos são usados para codificar suas respectivas propriedades MAPI no fluxo TNEF.</span><span class="sxs-lookup"><span data-stu-id="07f27-109">These attributes are used to encode their respective MAPI properties into the TNEF stream.</span></span> <span data-ttu-id="07f27-110">Além disso, um atributo especial é definido que pode ser usado para encapsular qualquer propriedade MAPI que não tenha um atributo específico correspondente a ela.</span><span class="sxs-lookup"><span data-stu-id="07f27-110">In addition, a special attribute is defined that can be used to encapsulate any MAPI property that does not have a specific attribute corresponding to it.</span></span> <span data-ttu-id="07f27-111">O motivo pelo qual esses atributos são definidos — em vez de simplesmente usar um método de codificação uniforme para todas as propriedades MAPI — é habilitar a compatibilidade com MAPI com software que está usando TNEF.</span><span class="sxs-lookup"><span data-stu-id="07f27-111">The reason these attributes are defined — instead of simply using a uniform encoding method for all MAPI properties — is to enable backward compatibility with non-MAPI-compliant software that is using TNEF.</span></span>
  
<span data-ttu-id="07f27-112">O restante desta seção descreve a estrutura e a sintaxe de um fluxo TNEF, o mapeamento entre propriedades MAPI e atributos TNEF e considerações importantes para determinados atributos TNEF.</span><span class="sxs-lookup"><span data-stu-id="07f27-112">The remainder of this section describes the structure and syntax of a TNEF stream, the mapping between MAPI properties and TNEF attributes, and important considerations for certain TNEF attributes.</span></span>
  

