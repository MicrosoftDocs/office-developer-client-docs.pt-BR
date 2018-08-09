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
description: '�ltima altera��o: s�bado, 23 de julho de 2011'
ms.openlocfilehash: a7bb1aca501e24843950114bb76b6a09b20f2467
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19767742"
---
# <a name="ixplogonaddresstypes"></a><span data-ttu-id="737e2-103">IXPLogon::AddressTypes</span><span class="sxs-lookup"><span data-stu-id="737e2-103">IXPLogon::AddressTypes</span></span>

  
  
<span data-ttu-id="737e2-104">**Aplica-se a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="737e2-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="737e2-105">Retorna os tipos de destinatários que processa o provedor de transporte.</span><span class="sxs-lookup"><span data-stu-id="737e2-105">Returns the types of recipients that the transport provider handles.</span></span>
  
```cpp
HRESULT AddressTypes(
  ULONG FAR * lpulFlags,
  ULONG FAR * lpcAdrType,
  LPSTR FAR * FAR * lpppszAdrTypeArray,
  ULONG FAR * lpcMAPIUID,
  LPUID FAR * FAR * lpppUIDArray
);
```

## <a name="parameters"></a><span data-ttu-id="737e2-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="737e2-106">Parameters</span></span>

 <span data-ttu-id="737e2-107">_lpulFlags_</span><span class="sxs-lookup"><span data-stu-id="737e2-107">_lpulFlags_</span></span>
  
> <span data-ttu-id="737e2-108">[out] Uma bitmask dos sinalizadores que controla o tipo de cadeias de caracteres retornada.</span><span class="sxs-lookup"><span data-stu-id="737e2-108">[out] A bitmask of flags that controls the type of strings returned.</span></span> <span data-ttu-id="737e2-109">O seguinte sinalizador pode ser definido:</span><span class="sxs-lookup"><span data-stu-id="737e2-109">The following flag can be set:</span></span>
    
<span data-ttu-id="737e2-110">MAPI_UNICODE</span><span class="sxs-lookup"><span data-stu-id="737e2-110">MAPI_UNICODE</span></span> 
  
> <span data-ttu-id="737e2-111">As cadeias de caracteres retornadas estão no formato Unicode.</span><span class="sxs-lookup"><span data-stu-id="737e2-111">The returned strings are in Unicode format.</span></span> <span data-ttu-id="737e2-112">Se o sinalizador MAPI_UNICODE não estiver definido, as cadeias de caracteres estão no formato ANSI.</span><span class="sxs-lookup"><span data-stu-id="737e2-112">If the MAPI_UNICODE flag is not set, the strings are in ANSI format.</span></span>
    
 <span data-ttu-id="737e2-113">_lpcAdrType_</span><span class="sxs-lookup"><span data-stu-id="737e2-113">_lpcAdrType_</span></span>
  
> <span data-ttu-id="737e2-114">[out] Um ponteiro para a contagem de entradas na matriz apontado pelo parâmetro _lpppszAdrTypeArray_ .</span><span class="sxs-lookup"><span data-stu-id="737e2-114">[out] A pointer to the count of entries in the array pointed to by the  _lpppszAdrTypeArray_ parameter.</span></span> 
    
 <span data-ttu-id="737e2-115">_lpppszAdrTypeArray_</span><span class="sxs-lookup"><span data-stu-id="737e2-115">_lpppszAdrTypeArray_</span></span>
  
> <span data-ttu-id="737e2-116">[out] Um ponteiro para um ponteiro para uma matriz de cadeias de caracteres que identificam os tipos de destinatário.</span><span class="sxs-lookup"><span data-stu-id="737e2-116">[out] A pointer to a pointer to an array of strings that identify recipient types.</span></span>
    
 <span data-ttu-id="737e2-117">_lpcMAPIUID_</span><span class="sxs-lookup"><span data-stu-id="737e2-117">_lpcMAPIUID_</span></span>
  
> <span data-ttu-id="737e2-118">[out] Um ponteiro para a contagem de entradas na matriz apontado pelo parâmetro _lpppUIDArray_ .</span><span class="sxs-lookup"><span data-stu-id="737e2-118">[out] A pointer to the count of entries in the array pointed to by the  _lpppUIDArray_ parameter.</span></span> 
    
 <span data-ttu-id="737e2-119">_lpppUIDArray_</span><span class="sxs-lookup"><span data-stu-id="737e2-119">_lpppUIDArray_</span></span>
  
> <span data-ttu-id="737e2-120">[out] Um ponteiro para um ponteiro para uma matriz de ponteiros para estruturas [MAPIUID](mapiuid.md) que identificam os tipos de destinatário.</span><span class="sxs-lookup"><span data-stu-id="737e2-120">[out] A pointer to a pointer to an array of pointers to [MAPIUID](mapiuid.md) structures that identify recipient types.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="737e2-121">Valor retornado</span><span class="sxs-lookup"><span data-stu-id="737e2-121">Return value</span></span>

<span data-ttu-id="737e2-122">S_OK</span><span class="sxs-lookup"><span data-stu-id="737e2-122">S_OK</span></span> 
  
> <span data-ttu-id="737e2-123">O provedor de transporte com êxito indicado os tipos de destinatários que pode manipular.</span><span class="sxs-lookup"><span data-stu-id="737e2-123">The transport provider successfully indicated the types of recipients that it can handle.</span></span>
    
## <a name="notes-to-implementers"></a><span data-ttu-id="737e2-124">Notas para implementadores</span><span class="sxs-lookup"><span data-stu-id="737e2-124">Notes to implementers</span></span>

<span data-ttu-id="737e2-125">O MAPI spooler chama o método de **IXPLogon::AddressTypes** imediatamente depois que um provedor de transporte retorna de uma chamada para o método [IXPProvider::TransportLogon](ixpprovider-transportlogon.md) para que o provedor de transporte pode indicar quais tipos de destinatários que ele manipula.</span><span class="sxs-lookup"><span data-stu-id="737e2-125">The MAPI spooler calls the **IXPLogon::AddressTypes** method immediately after a transport provider returns from a call to the [IXPProvider::TransportLogon](ixpprovider-transportlogon.md) method so the transport provider can indicate what types of recipients it handles.</span></span> <span data-ttu-id="737e2-126">Para indicar que isso, o provedor de transporte deve passar novamente no parâmetro _lpppszAdrTypeArray_ um ponteiro para uma matriz de ponteiros para as cadeias de caracteres ou passar novamente no parâmetro _lpppUIDArray_ um ponteiro para uma matriz de ponteiros para **MAPIUID** estruturas ou valores de passagem em ambos os parâmetros.</span><span class="sxs-lookup"><span data-stu-id="737e2-126">To indicate this, the transport provider should pass back in the  _lpppszAdrTypeArray_ parameter a pointer to an array of pointers to strings, or pass back in the  _lpppUIDArray_ parameter a pointer to an array of pointers to **MAPIUID** structures, or pass values in both parameters.</span></span> 
  
<span data-ttu-id="737e2-127">Essas duas matrizes são usados para processos de identificação diferente.</span><span class="sxs-lookup"><span data-stu-id="737e2-127">These two arrays are used for different identification processes.</span></span> <span data-ttu-id="737e2-128">MAPI e o MAPI spooler usam as estruturas [MAPIUID](mapiuid.md) na matriz _lpppUIDArray_ para identificar os identificadores de entrada do destinatário diretamente são manipulados pelo provedor de transporte ou pelo sistema de mensagens ao qual se conecta o provedor de transporte .</span><span class="sxs-lookup"><span data-stu-id="737e2-128">MAPI and the MAPI spooler use the [MAPIUID](mapiuid.md) structures in the  _lpppUIDArray_ array to identify those recipient entry identifiers that are directly handled by the transport provider or by the messaging system to which the transport provider connects.</span></span> <span data-ttu-id="737e2-129">Nem MAPI nem o MAPI spooler expande endereços usando identificadores de entrada contidos em qualquer uma dessas estruturas **MAPIUID** ; Essas estruturas são usadas apenas para a identificação do tipo de destinatário.</span><span class="sxs-lookup"><span data-stu-id="737e2-129">Neither MAPI nor the MAPI spooler expands addresses by using entry identifiers contained in any of these **MAPIUID** structures; these structures are used only for recipient type identification.</span></span> 
  
<span data-ttu-id="737e2-130">O MAPI spooler usa cada uma das cadeias de caracteres no parâmetro _lpppszAdrTypeArray_ para um teste de comparação quando ela decide qual provedor de transporte deve lidar com quais destinatários para uma mensagem de saída.</span><span class="sxs-lookup"><span data-stu-id="737e2-130">The MAPI spooler uses each of the strings in the  _lpppszAdrTypeArray_ parameter for a comparison test when it decides which transport provider should handle which recipients for an outbound message.</span></span> <span data-ttu-id="737e2-131">Se a propriedade de **PR_ADDRTYPE** ([PidTagAddressType](pidtagaddresstype-canonical-property.md)) de um destinatário de mensagem corresponde exatamente a uma cadeia de caracteres que identifica um dos tipos de endereço de mensagens que o provedor de transporte fornece, o provedor pode entregar a mensagem para que o destinatário.</span><span class="sxs-lookup"><span data-stu-id="737e2-131">If a message recipient's **PR_ADDRTYPE** ([PidTagAddressType](pidtagaddresstype-canonical-property.md)) property exactly matches a string that identifies one of the messaging address types that the transport provider supplies, the provider can deliver the message to that recipient.</span></span>
  
<span data-ttu-id="737e2-132">Se vários provedores de transporte podem lidar com o mesmo tipo de destinatário, MAPI seleciona um provedor de transporte com base na ordem de prioridade de transporte indicada no perfil do aplicativo cliente.</span><span class="sxs-lookup"><span data-stu-id="737e2-132">If multiple transport providers can handle the same type of recipient, MAPI selects a transport provider based on the transport priority order indicated in the client application's profile.</span></span> <span data-ttu-id="737e2-133">Para determinar qual provedor de transporte a ser usado, o MAPI spooler examina todas as estruturas **MAPIUID** provedor especificado em ordem de prioridade e, em seguida, todos os endereços especificados pelo provedor tipo valores em ordem de prioridade.</span><span class="sxs-lookup"><span data-stu-id="737e2-133">To determine which transport provider to use, the MAPI spooler scans all provider-specified **MAPIUID** structures in priority order, and then all provider-specified address type values in priority order.</span></span> <span data-ttu-id="737e2-134">O primeiro provedor de transporte para corresponder a um determinado destinatário neste exame obtém a primeira oportunidade para lidar com o destinatário.</span><span class="sxs-lookup"><span data-stu-id="737e2-134">The first transport provider to match a particular recipient in this scan gets the first opportunity to handle this recipient.</span></span> <span data-ttu-id="737e2-135">Se o provedor não manipular o destinatário, o MAPI spooler continua a varredura para localizar um provedor de transporte de qualquer destinatário ainda não foram tratado.</span><span class="sxs-lookup"><span data-stu-id="737e2-135">If that provider does not handle the recipient, the MAPI spooler continues the scan to find a transport provider for any recipient not yet handled.</span></span> <span data-ttu-id="737e2-136">O exame continua até que nenhuma correspondência adicional forem encontradas, nesse momento é gerado um relatório de não entrega para qualquer destinatário que não foi tratado.</span><span class="sxs-lookup"><span data-stu-id="737e2-136">The scan continues until no further matches are found, at which point a nondelivery report is generated for any recipient that was not handled.</span></span> 
  
<span data-ttu-id="737e2-137">Se o provedor sempre oferece suporte a um determinado conjunto de tipos de destinatário, o tipo de endereço e matrizes **MAPIUID** que o provedor de transporte passado podem ser estáticos.</span><span class="sxs-lookup"><span data-stu-id="737e2-137">If the provider always supports a particular set of recipient types, the address type and **MAPIUID** arrays that the transport provider passed can be static.</span></span> <span data-ttu-id="737e2-138">Se o provedor de transporte dinamicamente constrói desses conjuntos, ele pode alocar memória usando o objeto de suporte anteriormente passado na chamada a **TransportLogon**, embora isso não é necessário.</span><span class="sxs-lookup"><span data-stu-id="737e2-138">If the transport provider dynamically constructs these arrays, it can allocate memory by using the support object that was previously passed in the call to **TransportLogon**, although this is not necessary.</span></span>
  
<span data-ttu-id="737e2-139">A memória usada para o tipo de endereço e **MAPIUID** matrizes deve permanecer alocada até que a chamada final para o método [IXPLogon::TransportLogoff](ixplogon-transportlogoff.md) , no momento em que o provedor de transporte pode liberar a memória, se necessário.</span><span class="sxs-lookup"><span data-stu-id="737e2-139">The memory used for the address type and **MAPIUID** arrays should remain allocated until the final call to the [IXPLogon::TransportLogoff](ixplogon-transportlogoff.md) method, at which time the transport provider can free the memory, if necessary.</span></span> <span data-ttu-id="737e2-140">O provedor de transporte não deverá alterar o conteúdo desses conjuntos após ela retornar da chamada **TransportLogoff** .</span><span class="sxs-lookup"><span data-stu-id="737e2-140">The transport provider should not alter the contents of these arrays after it returns from the **TransportLogoff** call.</span></span> 
  
<span data-ttu-id="737e2-141">Um provedor de transporte que pode lidar com qualquer tipo de destinatário pode retornar NULL no parâmetro _lpppszAdrTypeArray_ .</span><span class="sxs-lookup"><span data-stu-id="737e2-141">A transport provider that can handle any type of recipient can return NULL in the  _lpppszAdrTypeArray_ parameter.</span></span> <span data-ttu-id="737e2-142">Provedores de transporte para sistemas de mensagens baseado em LAN que usa um servidor central para entregar mensagens enviadas para vários sistemas de mensagem estrangeira comumente fazer isso.</span><span class="sxs-lookup"><span data-stu-id="737e2-142">Transport providers for LAN-based messaging systems that use a central server to deliver outgoing messages to various foreign message systems commonly do this.</span></span> <span data-ttu-id="737e2-143">Esse tipo de provedor de transporte deve ser instalado por último na MAPI e MAPI ordem de prioridade de spooler de provedores de transporte no perfil.</span><span class="sxs-lookup"><span data-stu-id="737e2-143">This type of transport provider should be installed last in the MAPI and MAPI spooler priority order of transport providers in the profile.</span></span> 
  
<span data-ttu-id="737e2-144">Um provedor de transporte que não oferece suporte a mensagens de saída que são enviadas a ela com base no tipo de endereço deve retornar uma única cadeia de caracteres de comprimento zero em _lpppszAdrTypeArray_.</span><span class="sxs-lookup"><span data-stu-id="737e2-144">A transport provider that does not support outbound messages that are dispatched to it based on address type should return a single zero-length string in  _lpppszAdrTypeArray_.</span></span> <span data-ttu-id="737e2-145">Se um provedor de transporte não suporta nenhum tipo de destinatário, ele deve passar NULL para a estrutura **MAPIUID** e uma cadeia de caracteres vazia para o tipo de endereço.</span><span class="sxs-lookup"><span data-stu-id="737e2-145">If a transport provider supports no recipient types, it should pass NULL for the **MAPIUID** structure and an empty string for the address type.</span></span> <span data-ttu-id="737e2-146">Provedores de transporte desse tipo são mais comumente usadas para instalar um pré-processador de mensagem.</span><span class="sxs-lookup"><span data-stu-id="737e2-146">Transport providers of this type are most commonly used to install a message preprocessor.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="737e2-147">Confira também</span><span class="sxs-lookup"><span data-stu-id="737e2-147">See also</span></span>



[<span data-ttu-id="737e2-148">IXPLogon::TransportLogoff</span><span class="sxs-lookup"><span data-stu-id="737e2-148">IXPLogon::TransportLogoff</span></span>](ixplogon-transportlogoff.md)
  
[<span data-ttu-id="737e2-149">IXPProvider::TransportLogon</span><span class="sxs-lookup"><span data-stu-id="737e2-149">IXPProvider::TransportLogon</span></span>](ixpprovider-transportlogon.md)
  
[<span data-ttu-id="737e2-150">MAPIUID</span><span class="sxs-lookup"><span data-stu-id="737e2-150">MAPIUID</span></span>](mapiuid.md)
  
[<span data-ttu-id="737e2-151">IXPLogon : IUnknown</span><span class="sxs-lookup"><span data-stu-id="737e2-151">IXPLogon : IUnknown</span></span>](ixplogoniunknown.md)

