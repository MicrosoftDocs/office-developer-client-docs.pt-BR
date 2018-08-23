---
title: Comparar entradas do catálogo de endereços
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: e375367b-d107-4768-95de-00b8b9dc3511
description: '�ltima altera��o: s�bado, 23 de julho de 2011'
ms.openlocfilehash: e5c46aed7a15ae4f48c8e4f1fe308fcb20ab3fe7
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22575354"
---
# <a name="comparing-address-book-entries"></a><span data-ttu-id="6723b-103">Comparar entradas do catálogo de endereços</span><span class="sxs-lookup"><span data-stu-id="6723b-103">Comparing Address Book Entries</span></span>

  
  
<span data-ttu-id="6723b-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="6723b-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="6723b-105">Implementação de [IABLogon::CompareEntryIDs](iablogon-compareentryids.md) do seu provedor compara os identificadores de entrada para dois dos objetos do seu provedor.</span><span class="sxs-lookup"><span data-stu-id="6723b-105">Your provider's [IABLogon::CompareEntryIDs](iablogon-compareentryids.md) implementation compares the entry identifiers for two of your provider's objects.</span></span> <span data-ttu-id="6723b-106">MAPI chama esse método depois determinando se os identificadores de dois entrada contêm seu provedor registrado [MAPIUID](mapiuid.md).</span><span class="sxs-lookup"><span data-stu-id="6723b-106">MAPI calls this method after determining that the two entry identifiers contain your provider's registered [MAPIUID](mapiuid.md).</span></span> <span data-ttu-id="6723b-107">Portanto, seu método **CompareEntryIDs** não precisa verificar se os identificadores de entrada passados para os parâmetros _lpEntryID1_ e _lpEntryID2_ pertencem ao seu provedor.</span><span class="sxs-lookup"><span data-stu-id="6723b-107">Therefore, your **CompareEntryIDs** method need not check that the entry identifiers passed in for the  _lpEntryID1_ and  _lpEntryID2_ parameters belong to your provider.</span></span> 
  
<span data-ttu-id="6723b-108">Chamar **IABLogon::CompareEntryIDs** é equivalente a recuperar a propriedade **PR_RECORD_KEY** ([PidTagRecordKey](pidtagrecordkey-canonical-property.md)) para cada um dos dois objetos e compará-los diretamente.</span><span class="sxs-lookup"><span data-stu-id="6723b-108">Calling **IABLogon::CompareEntryIDs** is equivalent to retrieving the **PR_RECORD_KEY** ([PidTagRecordKey](pidtagrecordkey-canonical-property.md)) property for each of the two objects and comparing them directly.</span></span>
  
 <span data-ttu-id="6723b-109">**Para implementar CompareEntryIds**</span><span class="sxs-lookup"><span data-stu-id="6723b-109">**To implement CompareEntryIds**</span></span>
  
1. <span data-ttu-id="6723b-110">Verifique o tipo dos identificadores de entrada passados se seu provedor armazena essas informações.</span><span class="sxs-lookup"><span data-stu-id="6723b-110">Check the type of the entry identifiers passed in if your provider stores that information.</span></span> <span data-ttu-id="6723b-111">Por exemplo, um identificador de entrada pode pertencer a um usuário de mensagens, enquanto a outra pode pertencer a uma lista de distribuição.</span><span class="sxs-lookup"><span data-stu-id="6723b-111">For example, one entry identifier might belong to a messaging user while the other might belong to a distribution list.</span></span> <span data-ttu-id="6723b-112">Se os tipos não coincidirem, defina o conteúdo do parâmetro _lpulResult_ como FALSE e retorno.</span><span class="sxs-lookup"><span data-stu-id="6723b-112">If the types do not match, set the contents of the  _lpulResult_ parameter to FALSE and return.</span></span> 
    
2. <span data-ttu-id="6723b-113">Compare os tamanhos dos identificadores de entrada de dois.</span><span class="sxs-lookup"><span data-stu-id="6723b-113">Compare the sizes of the two entry identifiers.</span></span> <span data-ttu-id="6723b-114">Se não forem iguais, defina o conteúdo do parâmetro _lpulResult_ como FALSE e retorno.</span><span class="sxs-lookup"><span data-stu-id="6723b-114">If they are not the same, set the contents of the  _lpulResult_ parameter to FALSE and return.</span></span> 
    
3. <span data-ttu-id="6723b-115">Verifique se o tamanho dos identificadores de entrada é o tamanho correto para seu tipo.</span><span class="sxs-lookup"><span data-stu-id="6723b-115">Check that the size of the entry identifiers is the correct size for their type.</span></span> <span data-ttu-id="6723b-116">Caso contrário, defina o conteúdo do parâmetro _lpulResult_ como FALSE e retornar o valor de erro MAPI_E_UNKNOWN_ENTRYID.</span><span class="sxs-lookup"><span data-stu-id="6723b-116">If not, set the contents of the  _lpulResult_ parameter to FALSE and return the error value MAPI_E_UNKNOWN_ENTRYID.</span></span> 
    
4. <span data-ttu-id="6723b-117">Verifique se os identificadores de entrada são os mesmos.</span><span class="sxs-lookup"><span data-stu-id="6723b-117">Check if the entry identifiers are the same.</span></span> <span data-ttu-id="6723b-118">Se eles compararem igualmente, defina o conteúdo do parâmetro _lpulResult_ como TRUE e retorno.</span><span class="sxs-lookup"><span data-stu-id="6723b-118">If they compare equally, set the contents of the  _lpulResult_ parameter to TRUE and return.</span></span> <span data-ttu-id="6723b-119">Caso contrário, defina como FALSE antes de retornar.</span><span class="sxs-lookup"><span data-stu-id="6723b-119">Otherwise, set it to FALSE before returning.</span></span> 
    
5. <span data-ttu-id="6723b-120">Se seu provedor está comparando um identificador curto prazo de entrada com um identificador de longo prazo, eles devem compare igualmente.</span><span class="sxs-lookup"><span data-stu-id="6723b-120">If your provider is comparing a short-term entry identifier with a long-term identifier, they should compare equally.</span></span>
    

