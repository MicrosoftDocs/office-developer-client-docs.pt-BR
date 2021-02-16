---
title: Comparando entradas do Livro de Endereços
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: e375367b-d107-4768-95de-00b8b9dc3511
description: 'Última modificação: 23 de julho de 2011'
ms.openlocfilehash: 6ccd7a55c195b45b1fa83db6180efeacd41b968d
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33415352"
---
# <a name="comparing-address-book-entries"></a><span data-ttu-id="6edcb-103">Comparando entradas do Livro de Endereços</span><span class="sxs-lookup"><span data-stu-id="6edcb-103">Comparing Address Book Entries</span></span>

  
  
<span data-ttu-id="6edcb-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="6edcb-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="6edcb-105">A implementação de [IABLogon::CompareEntryIDs](iablogon-compareentryids.md) do provedor compara os identificadores de entrada de dois dos objetos do provedor.</span><span class="sxs-lookup"><span data-stu-id="6edcb-105">Your provider's [IABLogon::CompareEntryIDs](iablogon-compareentryids.md) implementation compares the entry identifiers for two of your provider's objects.</span></span> <span data-ttu-id="6edcb-106">MAPI calls this method after determining that the two entry identifiers contain your provider's registered [MAPIUID](mapiuid.md).</span><span class="sxs-lookup"><span data-stu-id="6edcb-106">MAPI calls this method after determining that the two entry identifiers contain your provider's registered [MAPIUID](mapiuid.md).</span></span> <span data-ttu-id="6edcb-107">Portanto, seu **método CompareEntryIDs** não precisa verificar se os identificadores de entrada passados para os parâmetros  _lpEntryID1_ e  _lpEntryID2_ pertencem ao seu provedor.</span><span class="sxs-lookup"><span data-stu-id="6edcb-107">Therefore, your **CompareEntryIDs** method need not check that the entry identifiers passed in for the  _lpEntryID1_ and  _lpEntryID2_ parameters belong to your provider.</span></span> 
  
<span data-ttu-id="6edcb-108">Chamar **IABLogon::CompareEntryIDs** é equivalente **a** recuperar a propriedade PR_RECORD_KEY ([PidTagRecordKey](pidtagrecordkey-canonical-property.md)) para cada um dos dois objetos e compará-los diretamente.</span><span class="sxs-lookup"><span data-stu-id="6edcb-108">Calling **IABLogon::CompareEntryIDs** is equivalent to retrieving the **PR_RECORD_KEY** ([PidTagRecordKey](pidtagrecordkey-canonical-property.md)) property for each of the two objects and comparing them directly.</span></span>
  
 <span data-ttu-id="6edcb-109">**Para implementar CompareEntryIds**</span><span class="sxs-lookup"><span data-stu-id="6edcb-109">**To implement CompareEntryIds**</span></span>
  
1. <span data-ttu-id="6edcb-110">Verifique o tipo dos identificadores de entrada passados se o provedor armazenar essas informações.</span><span class="sxs-lookup"><span data-stu-id="6edcb-110">Check the type of the entry identifiers passed in if your provider stores that information.</span></span> <span data-ttu-id="6edcb-111">Por exemplo, um identificador de entrada pode pertencer a um usuário de mensagens enquanto o outro pode pertencer a uma lista de distribuição.</span><span class="sxs-lookup"><span data-stu-id="6edcb-111">For example, one entry identifier might belong to a messaging user while the other might belong to a distribution list.</span></span> <span data-ttu-id="6edcb-112">Se os tipos não corresponderem, defina o conteúdo do parâmetro  _lpulResult_ como FALSE e retorne.</span><span class="sxs-lookup"><span data-stu-id="6edcb-112">If the types do not match, set the contents of the  _lpulResult_ parameter to FALSE and return.</span></span> 
    
2. <span data-ttu-id="6edcb-113">Compare os tamanhos dos dois identificadores de entrada.</span><span class="sxs-lookup"><span data-stu-id="6edcb-113">Compare the sizes of the two entry identifiers.</span></span> <span data-ttu-id="6edcb-114">Se eles não são os mesmos, defina o conteúdo do parâmetro  _lpulResult_ como FALSE e retorne.</span><span class="sxs-lookup"><span data-stu-id="6edcb-114">If they are not the same, set the contents of the  _lpulResult_ parameter to FALSE and return.</span></span> 
    
3. <span data-ttu-id="6edcb-115">Verifique se o tamanho dos identificadores de entrada é o tamanho correto para seu tipo.</span><span class="sxs-lookup"><span data-stu-id="6edcb-115">Check that the size of the entry identifiers is the correct size for their type.</span></span> <span data-ttu-id="6edcb-116">Se não estiver, defina o conteúdo do parâmetro  _lpulResult_ como FALSE e retorne o valor de erro MAPI_E_UNKNOWN_ENTRYID.</span><span class="sxs-lookup"><span data-stu-id="6edcb-116">If not, set the contents of the  _lpulResult_ parameter to FALSE and return the error value MAPI_E_UNKNOWN_ENTRYID.</span></span> 
    
4. <span data-ttu-id="6edcb-117">Verifique se os identificadores de entrada são os mesmos.</span><span class="sxs-lookup"><span data-stu-id="6edcb-117">Check if the entry identifiers are the same.</span></span> <span data-ttu-id="6edcb-118">Se compararem igualmente, defina o conteúdo do parâmetro  _lpulResult_ como VERDADEIRO e retorne.</span><span class="sxs-lookup"><span data-stu-id="6edcb-118">If they compare equally, set the contents of the  _lpulResult_ parameter to TRUE and return.</span></span> <span data-ttu-id="6edcb-119">Caso contrário, de definida como FALSE antes de retornar.</span><span class="sxs-lookup"><span data-stu-id="6edcb-119">Otherwise, set it to FALSE before returning.</span></span> 
    
5. <span data-ttu-id="6edcb-120">Se o provedor estiver comparando um identificador de entrada de curto prazo com um identificador de longo prazo, ele deverá comparar igualmente.</span><span class="sxs-lookup"><span data-stu-id="6edcb-120">If your provider is comparing a short-term entry identifier with a long-term identifier, they should compare equally.</span></span>
    

