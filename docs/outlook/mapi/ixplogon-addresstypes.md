---
title: IXPLogonAddressTypes
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IXPLogon.AddressTypes
api_type:
- COM
ms.assetid: 5add1f2b-d9e6-4d78-8739-c3848f6e32a3
description: 'Última modificação: 23 de julho de 2011'
ms.openlocfilehash: ca68c604152a7a28fb6a5357aa9c012ec7466b5a
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32357208"
---
# <a name="ixplogonaddresstypes"></a><span data-ttu-id="9e515-103">IXPLogon::AddressTypes</span><span class="sxs-lookup"><span data-stu-id="9e515-103">IXPLogon::AddressTypes</span></span>

  
  
<span data-ttu-id="9e515-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="9e515-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="9e515-105">Retorna os tipos de destinatários que o provedor de transporte manipula.</span><span class="sxs-lookup"><span data-stu-id="9e515-105">Returns the types of recipients that the transport provider handles.</span></span>
  
```cpp
HRESULT AddressTypes(
  ULONG FAR * lpulFlags,
  ULONG FAR * lpcAdrType,
  LPSTR FAR * FAR * lpppszAdrTypeArray,
  ULONG FAR * lpcMAPIUID,
  LPUID FAR * FAR * lpppUIDArray
);
```

## <a name="parameters"></a><span data-ttu-id="9e515-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="9e515-106">Parameters</span></span>

 <span data-ttu-id="9e515-107">_lpulFlags_</span><span class="sxs-lookup"><span data-stu-id="9e515-107">_lpulFlags_</span></span>
  
> <span data-ttu-id="9e515-108">bota Uma bitmask de sinalizadores que controla o tipo de cadeia de caracteres retornada.</span><span class="sxs-lookup"><span data-stu-id="9e515-108">[out] A bitmask of flags that controls the type of strings returned.</span></span> <span data-ttu-id="9e515-109">O seguinte sinalizador pode ser definido:</span><span class="sxs-lookup"><span data-stu-id="9e515-109">The following flag can be set:</span></span>
    
<span data-ttu-id="9e515-110">MAPI_UNICODE</span><span class="sxs-lookup"><span data-stu-id="9e515-110">MAPI_UNICODE</span></span> 
  
> <span data-ttu-id="9e515-111">As cadeias de caracteres retornadas estão no formato Unicode.</span><span class="sxs-lookup"><span data-stu-id="9e515-111">The returned strings are in Unicode format.</span></span> <span data-ttu-id="9e515-112">Se o sinalizador MAPI_UNICODE não estiver definido, as cadeias de caracteres estarão no formato ANSI.</span><span class="sxs-lookup"><span data-stu-id="9e515-112">If the MAPI_UNICODE flag is not set, the strings are in ANSI format.</span></span>
    
 <span data-ttu-id="9e515-113">_lpcAdrType_</span><span class="sxs-lookup"><span data-stu-id="9e515-113">_lpcAdrType_</span></span>
  
> <span data-ttu-id="9e515-114">bota Um ponteiro para a contagem de entradas na matriz apontada pelo parâmetro _lpppszAdrTypeArray_ .</span><span class="sxs-lookup"><span data-stu-id="9e515-114">[out] A pointer to the count of entries in the array pointed to by the  _lpppszAdrTypeArray_ parameter.</span></span> 
    
 <span data-ttu-id="9e515-115">_lpppszAdrTypeArray_</span><span class="sxs-lookup"><span data-stu-id="9e515-115">_lpppszAdrTypeArray_</span></span>
  
> <span data-ttu-id="9e515-116">bota Um ponteiro para um ponteiro para uma matriz de cadeias de caracteres que identificam tipos de destinatários.</span><span class="sxs-lookup"><span data-stu-id="9e515-116">[out] A pointer to a pointer to an array of strings that identify recipient types.</span></span>
    
 <span data-ttu-id="9e515-117">_lpcMAPIUID_</span><span class="sxs-lookup"><span data-stu-id="9e515-117">_lpcMAPIUID_</span></span>
  
> <span data-ttu-id="9e515-118">bota Um ponteiro para a contagem de entradas na matriz apontada pelo parâmetro _lpppUIDArray_ .</span><span class="sxs-lookup"><span data-stu-id="9e515-118">[out] A pointer to the count of entries in the array pointed to by the  _lpppUIDArray_ parameter.</span></span> 
    
 <span data-ttu-id="9e515-119">_lpppUIDArray_</span><span class="sxs-lookup"><span data-stu-id="9e515-119">_lpppUIDArray_</span></span>
  
> <span data-ttu-id="9e515-120">bota Um ponteiro para um ponteiro para uma matriz de ponteiros para estruturas [MAPIUID](mapiuid.md) que identificam os tipos de destinatários.</span><span class="sxs-lookup"><span data-stu-id="9e515-120">[out] A pointer to a pointer to an array of pointers to [MAPIUID](mapiuid.md) structures that identify recipient types.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="9e515-121">Valor de retorno</span><span class="sxs-lookup"><span data-stu-id="9e515-121">Return value</span></span>

<span data-ttu-id="9e515-122">S_OK</span><span class="sxs-lookup"><span data-stu-id="9e515-122">S_OK</span></span> 
  
> <span data-ttu-id="9e515-123">O provedor de transporte indicou com êxito os tipos de destinatários que ele pode manipular.</span><span class="sxs-lookup"><span data-stu-id="9e515-123">The transport provider successfully indicated the types of recipients that it can handle.</span></span>
    
## <a name="notes-to-implementers"></a><span data-ttu-id="9e515-124">Observações para implementadores</span><span class="sxs-lookup"><span data-stu-id="9e515-124">Notes to implementers</span></span>

<span data-ttu-id="9e515-125">O spooler MAPI chama o método **IXPLogon:: AddressTypes** imediatamente após um provedor de transporte retornar de uma chamada para o método [IXPProvider:: TransportLogon](ixpprovider-transportlogon.md) para que o provedor de transporte possa indicar quais tipos de destinatários ele manipula.</span><span class="sxs-lookup"><span data-stu-id="9e515-125">The MAPI spooler calls the **IXPLogon::AddressTypes** method immediately after a transport provider returns from a call to the [IXPProvider::TransportLogon](ixpprovider-transportlogon.md) method so the transport provider can indicate what types of recipients it handles.</span></span> <span data-ttu-id="9e515-126">Para indicar isso, o provedor de transporte deve passar de volta no parâmetro _lpppszAdrTypeArray_ um ponteiro para uma matriz de ponteiros para cadeias de caracteres ou passar de volta no parâmetro _lpppUIDArray_ um ponteiro para uma matriz de ponteiros para **MAPIUID** estruturas ou valores de passagem em ambos os parâmetros.</span><span class="sxs-lookup"><span data-stu-id="9e515-126">To indicate this, the transport provider should pass back in the  _lpppszAdrTypeArray_ parameter a pointer to an array of pointers to strings, or pass back in the  _lpppUIDArray_ parameter a pointer to an array of pointers to **MAPIUID** structures, or pass values in both parameters.</span></span> 
  
<span data-ttu-id="9e515-127">Essas duas matrizes são usadas para diferentes processos de identificação.</span><span class="sxs-lookup"><span data-stu-id="9e515-127">These two arrays are used for different identification processes.</span></span> <span data-ttu-id="9e515-128">O MAPI e o spooler MAPI usam as estruturas [MAPIUID](mapiuid.md) na matriz _lpppUIDArray_ para identificar os identificadores de entrada de destinatários diretamente tratados pelo provedor de transporte ou pelo sistema de mensagens ao qual o provedor de transporte se conecta .</span><span class="sxs-lookup"><span data-stu-id="9e515-128">MAPI and the MAPI spooler use the [MAPIUID](mapiuid.md) structures in the  _lpppUIDArray_ array to identify those recipient entry identifiers that are directly handled by the transport provider or by the messaging system to which the transport provider connects.</span></span> <span data-ttu-id="9e515-129">Nem o MAPI nem o spooler MAPI expandem endereços usando identificadores de entrada contidos em qualquer uma dessas estruturas **MAPIUID** ; essas estruturas são usadas apenas para identificação de tipo de destinatário.</span><span class="sxs-lookup"><span data-stu-id="9e515-129">Neither MAPI nor the MAPI spooler expands addresses by using entry identifiers contained in any of these **MAPIUID** structures; these structures are used only for recipient type identification.</span></span> 
  
<span data-ttu-id="9e515-130">O spooler MAPI usa cada cadeia de caracteres no parâmetro _lpppszAdrTypeArray_ para um teste de comparação quando decide qual provedor de transporte deve lidar com os destinatários de uma mensagem de saída.</span><span class="sxs-lookup"><span data-stu-id="9e515-130">The MAPI spooler uses each of the strings in the  _lpppszAdrTypeArray_ parameter for a comparison test when it decides which transport provider should handle which recipients for an outbound message.</span></span> <span data-ttu-id="9e515-131">Se a propriedade **PR_ADDRTYPE** ([PidTagAddressType](pidtagaddresstype-canonical-property.md)) de um destinatário de mensagem corresponder exatamente a uma cadeia de caracteres que identifica um dos tipos de endereço de mensagens que o provedor de transporte fornece, o provedor poderá entregar a mensagem para esse destinatário.</span><span class="sxs-lookup"><span data-stu-id="9e515-131">If a message recipient's **PR_ADDRTYPE** ([PidTagAddressType](pidtagaddresstype-canonical-property.md)) property exactly matches a string that identifies one of the messaging address types that the transport provider supplies, the provider can deliver the message to that recipient.</span></span>
  
<span data-ttu-id="9e515-132">Se vários provedores de transporte puderem lidar com o mesmo tipo de destinatário, MAPI selecionará um provedor de transporte com base na ordem de prioridade de transporte indicada no perfil do aplicativo cliente.</span><span class="sxs-lookup"><span data-stu-id="9e515-132">If multiple transport providers can handle the same type of recipient, MAPI selects a transport provider based on the transport priority order indicated in the client application's profile.</span></span> <span data-ttu-id="9e515-133">Para determinar qual provedor de transporte usar, o spooler MAPI examina todas as estruturas **MAPIUID** especificadas pelo provedor em ordem de prioridade e, em seguida, todos os valores de tipo de endereço especificados por provedor em ordem de prioridade.</span><span class="sxs-lookup"><span data-stu-id="9e515-133">To determine which transport provider to use, the MAPI spooler scans all provider-specified **MAPIUID** structures in priority order, and then all provider-specified address type values in priority order.</span></span> <span data-ttu-id="9e515-134">O primeiro provedor de transporte a corresponder a um determinado destinatário nesta verificação Obtém a primeira oportunidade para lidar com esse destinatário.</span><span class="sxs-lookup"><span data-stu-id="9e515-134">The first transport provider to match a particular recipient in this scan gets the first opportunity to handle this recipient.</span></span> <span data-ttu-id="9e515-135">Se esse provedor não manipular o destinatário, o spooler MAPI continuará a examinar para localizar um provedor de transporte para qualquer destinatário ainda não tratado.</span><span class="sxs-lookup"><span data-stu-id="9e515-135">If that provider does not handle the recipient, the MAPI spooler continues the scan to find a transport provider for any recipient not yet handled.</span></span> <span data-ttu-id="9e515-136">A verificação continua até que nenhuma outra correspondência seja encontrada, no ponto em que um relatório de não entrega é gerado para qualquer destinatário que não tenha sido manipulado.</span><span class="sxs-lookup"><span data-stu-id="9e515-136">The scan continues until no further matches are found, at which point a nondelivery report is generated for any recipient that was not handled.</span></span> 
  
<span data-ttu-id="9e515-137">Se o provedor oferecer suporte a um determinado conjunto de tipos de destinatários, o tipo de endereço e as matrizes do **MAPIUID** que o provedor de transporte transmitir poderão ser estáticas.</span><span class="sxs-lookup"><span data-stu-id="9e515-137">If the provider always supports a particular set of recipient types, the address type and **MAPIUID** arrays that the transport provider passed can be static.</span></span> <span data-ttu-id="9e515-138">Se o provedor de transporte cria dinamicamente essas matrizes, ele pode alocar memória usando o objeto support que foi passado anteriormente na chamada para **TransportLogon**, embora isso não seja necessário.</span><span class="sxs-lookup"><span data-stu-id="9e515-138">If the transport provider dynamically constructs these arrays, it can allocate memory by using the support object that was previously passed in the call to **TransportLogon**, although this is not necessary.</span></span>
  
<span data-ttu-id="9e515-139">A memória usada para o tipo de endereço e matrizes **MAPIUID** deve permanecer alocada até a chamada final para o método [IXPLogon:: TransportLogoff](ixplogon-transportlogoff.md) , no momento em que o provedor de transporte pode liberar a memória, se necessário.</span><span class="sxs-lookup"><span data-stu-id="9e515-139">The memory used for the address type and **MAPIUID** arrays should remain allocated until the final call to the [IXPLogon::TransportLogoff](ixplogon-transportlogoff.md) method, at which time the transport provider can free the memory, if necessary.</span></span> <span data-ttu-id="9e515-140">O provedor de transporte não deve alterar o conteúdo dessas matrizes depois de retornar da chamada **TransportLogoff** .</span><span class="sxs-lookup"><span data-stu-id="9e515-140">The transport provider should not alter the contents of these arrays after it returns from the **TransportLogoff** call.</span></span> 
  
<span data-ttu-id="9e515-141">Um provedor de transporte que pode manipular qualquer tipo de destinatário pode retornar NULL no parâmetro _lpppszAdrTypeArray_ .</span><span class="sxs-lookup"><span data-stu-id="9e515-141">A transport provider that can handle any type of recipient can return NULL in the  _lpppszAdrTypeArray_ parameter.</span></span> <span data-ttu-id="9e515-142">Provedores de transporte para sistemas de mensagens baseados em LAN que usam um servidor central para entregar mensagens de saída a vários sistemas de mensagens externos normalmente fazem isso.</span><span class="sxs-lookup"><span data-stu-id="9e515-142">Transport providers for LAN-based messaging systems that use a central server to deliver outgoing messages to various foreign message systems commonly do this.</span></span> <span data-ttu-id="9e515-143">Esse tipo de provedor de transporte deve ser instalado por último na ordem de prioridade de MAPI e spooler MAPI dos provedores de transporte no perfil.</span><span class="sxs-lookup"><span data-stu-id="9e515-143">This type of transport provider should be installed last in the MAPI and MAPI spooler priority order of transport providers in the profile.</span></span> 
  
<span data-ttu-id="9e515-144">Um provedor de transporte que não oferece suporte a mensagens de saída que foram despachadas com base no tipo de endereço deve retornar uma única sequência de comprimento zero no _lpppszAdrTypeArray_.</span><span class="sxs-lookup"><span data-stu-id="9e515-144">A transport provider that does not support outbound messages that are dispatched to it based on address type should return a single zero-length string in  _lpppszAdrTypeArray_.</span></span> <span data-ttu-id="9e515-145">Se um provedor de transporte não oferecer suporte a tipos de destinatários, ele deverá passar NULL para a estrutura **MAPIUID** e uma cadeia de caracteres vazia para o tipo de endereço.</span><span class="sxs-lookup"><span data-stu-id="9e515-145">If a transport provider supports no recipient types, it should pass NULL for the **MAPIUID** structure and an empty string for the address type.</span></span> <span data-ttu-id="9e515-146">Provedores de transporte desse tipo são usados com mais frequência para instalar um pré-processador de mensagem.</span><span class="sxs-lookup"><span data-stu-id="9e515-146">Transport providers of this type are most commonly used to install a message preprocessor.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="9e515-147">Confira também</span><span class="sxs-lookup"><span data-stu-id="9e515-147">See also</span></span>



[<span data-ttu-id="9e515-148">IXPLogon::TransportLogoff</span><span class="sxs-lookup"><span data-stu-id="9e515-148">IXPLogon::TransportLogoff</span></span>](ixplogon-transportlogoff.md)
  
[<span data-ttu-id="9e515-149">IXPProvider::TransportLogon</span><span class="sxs-lookup"><span data-stu-id="9e515-149">IXPProvider::TransportLogon</span></span>](ixpprovider-transportlogon.md)
  
[<span data-ttu-id="9e515-150">MAPIUID</span><span class="sxs-lookup"><span data-stu-id="9e515-150">MAPIUID</span></span>](mapiuid.md)
  
[<span data-ttu-id="9e515-151">IXPLogon : IUnknown</span><span class="sxs-lookup"><span data-stu-id="9e515-151">IXPLogon : IUnknown</span></span>](ixplogoniunknown.md)

