---
title: ENTRYID
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.ENTRYID
api_type:
- COM
ms.assetid: 8ebb21ca-5ad1-4dcc-97b6-2390664b5d8d
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: c77acb5226361ce31a7f6b1694de7fe23f8dd71b
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33415268"
---
# <a name="entryid"></a><span data-ttu-id="2b737-103">ENTRYID</span><span class="sxs-lookup"><span data-stu-id="2b737-103">ENTRYID</span></span>

  
  
<span data-ttu-id="2b737-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="2b737-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="2b737-105">Contém um identificador de entrada para um objeto MAPI.</span><span class="sxs-lookup"><span data-stu-id="2b737-105">Contains an entry identifier for a MAPI object.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="2b737-106">Arquivo de cabeçalho:</span><span class="sxs-lookup"><span data-stu-id="2b737-106">Header file:</span></span>  <br/> |<span data-ttu-id="2b737-107">Mapidefs. h</span><span class="sxs-lookup"><span data-stu-id="2b737-107">Mapidefs.h</span></span>  <br/> |
|<span data-ttu-id="2b737-108">Macros relacionadas:</span><span class="sxs-lookup"><span data-stu-id="2b737-108">Related macros:</span></span>  <br/> |<span data-ttu-id="2b737-109">[CbNewENTRYID](cbnewentryid.md), [SizedENTRYID](sizedentryid.md)</span><span class="sxs-lookup"><span data-stu-id="2b737-109">[CbNewENTRYID](cbnewentryid.md), [SizedENTRYID](sizedentryid.md)</span></span> <br/> |
   
```cpp
typedef struct
{
  BYTE abFlags[4];
  BYTE ab[MAPI_DIM];
} ENTRYID, FAR *LPENTRYID;

```

## <a name="members"></a><span data-ttu-id="2b737-110">Members</span><span class="sxs-lookup"><span data-stu-id="2b737-110">Members</span></span>

 <span data-ttu-id="2b737-111">**abFlags**</span><span class="sxs-lookup"><span data-stu-id="2b737-111">**abFlags**</span></span>
  
> <span data-ttu-id="2b737-112">Bitmask de sinalizadores que fornecem informações que descrevem o objeto.</span><span class="sxs-lookup"><span data-stu-id="2b737-112">Bitmask of flags that provide information that describes the object.</span></span> <span data-ttu-id="2b737-113">Somente o primeiro byte dos sinalizadores, **abFlags [0]**, pode ser definido pelo provedor; os outros três são reservados.</span><span class="sxs-lookup"><span data-stu-id="2b737-113">Only the first byte of the flags, **abFlags[0]**, may be set by the provider; the other three are reserved.</span></span> <span data-ttu-id="2b737-114">Esses sinalizadores não devem ser definidos para identificadores de entradas permanentes; Eles são definidos apenas para identificadores de entrada de curto prazo.</span><span class="sxs-lookup"><span data-stu-id="2b737-114">These flags must not be set for permanent entry identifiers; they are only set for short-term entry identifiers.</span></span> <span data-ttu-id="2b737-115">Para clientes, essa estrutura é somente leitura.</span><span class="sxs-lookup"><span data-stu-id="2b737-115">To clients, this structure is read-only.</span></span> <span data-ttu-id="2b737-116">Os seguintes sinalizadores podem ser definidos no **abFlags [0]**:</span><span class="sxs-lookup"><span data-stu-id="2b737-116">The following flags can be set in **abFlags[0]**:</span></span>
    
<span data-ttu-id="2b737-117">MAPI_NOTRECIP</span><span class="sxs-lookup"><span data-stu-id="2b737-117">MAPI_NOTRECIP</span></span> 
  
> <span data-ttu-id="2b737-118">O identificador de entrada não pode ser usado como um destinatário em uma mensagem.</span><span class="sxs-lookup"><span data-stu-id="2b737-118">The entry identifier cannot be used as a recipient on a message.</span></span>
    
<span data-ttu-id="2b737-119">MAPI_NOTRESERVED</span><span class="sxs-lookup"><span data-stu-id="2b737-119">MAPI_NOTRESERVED</span></span> 
  
> <span data-ttu-id="2b737-120">Outros usuários não podem acessar o identificador de entrada.</span><span class="sxs-lookup"><span data-stu-id="2b737-120">Other users cannot access the entry identifier.</span></span>
    
<span data-ttu-id="2b737-121">MAPI_NOW</span><span class="sxs-lookup"><span data-stu-id="2b737-121">MAPI_NOW</span></span> 
  
> <span data-ttu-id="2b737-122">O identificador de entrada não pode ser usado em outros momentos.</span><span class="sxs-lookup"><span data-stu-id="2b737-122">The entry identifier cannot be used at other times.</span></span>
    
<span data-ttu-id="2b737-123">MAPI_SHORTTERM</span><span class="sxs-lookup"><span data-stu-id="2b737-123">MAPI_SHORTTERM</span></span> 
  
> <span data-ttu-id="2b737-124">O identificador de entrada é de curto prazo.</span><span class="sxs-lookup"><span data-stu-id="2b737-124">The entry identifier is short-term.</span></span> <span data-ttu-id="2b737-125">Todos os outros valores nesse byte devem ser definidos, a menos que outros usos do identificador de entrada estejam habilitados.</span><span class="sxs-lookup"><span data-stu-id="2b737-125">All other values in this byte must be set unless other uses of the entry identifier are enabled.</span></span>
    
<span data-ttu-id="2b737-126">MAPI_THISSESSION</span><span class="sxs-lookup"><span data-stu-id="2b737-126">MAPI_THISSESSION</span></span> 
  
> <span data-ttu-id="2b737-127">O identificador de entrada não pode ser usado em outras sessões.</span><span class="sxs-lookup"><span data-stu-id="2b737-127">The entry identifier cannot be used on other sessions.</span></span>
    
 <span data-ttu-id="2b737-128">**AB**</span><span class="sxs-lookup"><span data-stu-id="2b737-128">**ab**</span></span>
  
> <span data-ttu-id="2b737-129">Indica uma matriz de dados binários que é usada por provedores de serviços.</span><span class="sxs-lookup"><span data-stu-id="2b737-129">Indicates an array of binary data that is used by service providers.</span></span> <span data-ttu-id="2b737-130">O aplicativo cliente não pode usar essa matriz.</span><span class="sxs-lookup"><span data-stu-id="2b737-130">The client application cannot use this array.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="2b737-131">Comentários</span><span class="sxs-lookup"><span data-stu-id="2b737-131">Remarks</span></span>

<span data-ttu-id="2b737-132">A \*\*\*\* estrutura ENTRYID é usada por provedores de repositório de mensagens e de catálogo de endereços para construir identificadores exclusivos para seus objetos.</span><span class="sxs-lookup"><span data-stu-id="2b737-132">The **ENTRYID** structure is used by message store and address book providers to construct unique identifiers for their objects.</span></span> <span data-ttu-id="2b737-133">Os identificadores de entrada são usados para identificar os seguintes tipos de objetos:</span><span class="sxs-lookup"><span data-stu-id="2b737-133">Entry identifiers are used to identify the following types of objects:</span></span> 
  
- <span data-ttu-id="2b737-134">Repositórios de mensagens</span><span class="sxs-lookup"><span data-stu-id="2b737-134">Message stores</span></span>
    
- <span data-ttu-id="2b737-135">Folders</span><span class="sxs-lookup"><span data-stu-id="2b737-135">Folders</span></span>
    
- <span data-ttu-id="2b737-136">Mensagens</span><span class="sxs-lookup"><span data-stu-id="2b737-136">Messages</span></span>
    
- <span data-ttu-id="2b737-137">Contêineres do catálogo de endereços</span><span class="sxs-lookup"><span data-stu-id="2b737-137">Address book containers</span></span>
    
- <span data-ttu-id="2b737-138">Listas de distribuição</span><span class="sxs-lookup"><span data-stu-id="2b737-138">Distribution lists</span></span>
    
- <span data-ttu-id="2b737-139">Usuários de mensagens</span><span class="sxs-lookup"><span data-stu-id="2b737-139">Messaging users</span></span>
    
- <span data-ttu-id="2b737-140">Objetos de status</span><span class="sxs-lookup"><span data-stu-id="2b737-140">Status objects</span></span>
    
- <span data-ttu-id="2b737-141">Seções de perfil</span><span class="sxs-lookup"><span data-stu-id="2b737-141">Profile sections</span></span>
    
<span data-ttu-id="2b737-142">Cada provedor usa um formato para a \*\*\*\* estrutura ENTRYID que faz sentido para esse provedor.</span><span class="sxs-lookup"><span data-stu-id="2b737-142">Each provider uses a format for the **ENTRYID** structure that makes sense for that provider.</span></span> 
  
<span data-ttu-id="2b737-143">Os identificadores de entrada não podem ser comparados diretamente porque um objeto pode ser representado por dois valores binários diferentes.</span><span class="sxs-lookup"><span data-stu-id="2b737-143">Entry identifiers cannot be compared directly because one object can be represented by two different binary values.</span></span> <span data-ttu-id="2b737-144">Para determinar se dois identificadores de entrada representam o mesmo objeto, chame o método [IMAPISession:: CompareEntryIDs](imapisession-compareentryids.md) .</span><span class="sxs-lookup"><span data-stu-id="2b737-144">To determine whether two entry identifiers represent the same object, call the [IMAPISession::CompareEntryIDs](imapisession-compareentryids.md) method.</span></span> 
  
<span data-ttu-id="2b737-145">Quando um cliente chama o método [IMAPIProp::](imapiprop-getprops.md) GetProps de um objeto para recuperar seu identificador de entrada, o objeto retorna a forma mais permanente do identificador de entrada.</span><span class="sxs-lookup"><span data-stu-id="2b737-145">When a client calls an object's [IMAPIProp::GetProps](imapiprop-getprops.md) method to retrieve its entry identifier, the object returns the most permanent form of the entry identifier.</span></span> <span data-ttu-id="2b737-146">Um cliente pode verificar se um identificador de entrada é de longo prazo, verificando se nenhum dos sinalizadores está definido no primeiro byte do membro **abFlags** .</span><span class="sxs-lookup"><span data-stu-id="2b737-146">A client can verify that an entry identifier is long-term by checking that none of the flags are set in the first byte of the **abFlags** member.</span></span> 
  
<span data-ttu-id="2b737-147">Quando um cliente acessa um identificador de entrada por meio de uma coluna em uma tabela, provavelmente esse identificador de entrada é de curto prazo em vez de longo prazo.</span><span class="sxs-lookup"><span data-stu-id="2b737-147">When a client accesses an entry identifier through a column in a table, most likely this entry identifier is short-term instead of long-term.</span></span> <span data-ttu-id="2b737-148">Identificadores de entrada de curto prazo podem ser usados para abrir seus objetos correspondentes apenas na sessão MAPI atual.</span><span class="sxs-lookup"><span data-stu-id="2b737-148">Short-term entry identifiers can be used to open their corresponding objects only in the current MAPI session.</span></span> <span data-ttu-id="2b737-149">Um cliente pode verificar se um identificador de entrada é de curto prazo verificando se todos os sinalizadores estão definidos no primeiro byte do membro **abFlags** .</span><span class="sxs-lookup"><span data-stu-id="2b737-149">A client can verify that an entry identifier is short-term by checking that all of the flags are set in the first byte of the **abFlags** member.</span></span> 
  
<span data-ttu-id="2b737-150">Alguns identificadores de entrada são de curto prazo, mas têm uso de longo prazo.</span><span class="sxs-lookup"><span data-stu-id="2b737-150">Some entry identifiers are short-term, but have long-term use.</span></span> <span data-ttu-id="2b737-151">Esse identificador de entrada terá um ou mais dos sinalizadores apropriados definidos no primeiro byte de seu membro **abFlags** .</span><span class="sxs-lookup"><span data-stu-id="2b737-151">Such an entry identifier will have one or more of the appropriate flags set in the first byte of its **abFlags** member.</span></span> 
  
<span data-ttu-id="2b737-152">Uma \*\*\*\* estrutura ENTRYID é semelhante a uma estrutura [FLATENTRY](flatentry.md) .</span><span class="sxs-lookup"><span data-stu-id="2b737-152">An **ENTRYID** structure resembles a [FLATENTRY](flatentry.md) structure.</span></span> <span data-ttu-id="2b737-153">No enTanto, há algumas diferenças:</span><span class="sxs-lookup"><span data-stu-id="2b737-153">However, there are some differences:</span></span> 
  
- <span data-ttu-id="2b737-154">Uma \*\*\*\* estrutura ENTRYID não armazena o tamanho do identificador de entrada; uma estrutura **FLATENTRY** .</span><span class="sxs-lookup"><span data-stu-id="2b737-154">An **ENTRYID** structure does not store the size of the entry identifier; a **FLATENTRY** structure does.</span></span> 
    
- <span data-ttu-id="2b737-155">Uma \*\*\*\* estrutura ENTRYID armazena os dados de sinalizador e o restante do identificador de entrada separadamente; uma estrutura **FLATENTRY** armazena os dados de sinalizador com o resto do identificador de entrada.</span><span class="sxs-lookup"><span data-stu-id="2b737-155">An **ENTRYID** structure stores the flag data and the rest of the entry identifier separately; a **FLATENTRY** structure stores the flag data with the rest of the entry identifier.</span></span> 
    
- <span data-ttu-id="2b737-156">Uma \*\*\*\* estrutura ENTRYID é passada como um parâmetro para os métodos da interface [IMAPIProp](imapipropiunknown.md) e para os seguintes métodos **OpenEntry** : [IABLogon:: OpenEntry](iablogon-openentry.md), [IAddrBook:: OpenEntry](iaddrbook-openentry.md), [IMAPIContainer:: OpenEntry ](imapicontainer-openentry.md), [IMAPISession:: OpenEntry](imapisession-openentry.md), [IMAPISupport:: OpenEntry](imapisupport-openentry.md), [IMsgStore:: OpenEntry](imsgstore-openentry.md), [IMSLogon::](imslogon-openentry.md) OpenEntry</span><span class="sxs-lookup"><span data-stu-id="2b737-156">An **ENTRYID** structure is passed as a parameter to the methods of the [IMAPIProp](imapipropiunknown.md) interface and to the following **OpenEntry** methods: [IABLogon::OpenEntry](iablogon-openentry.md), [IAddrBook::OpenEntry](iaddrbook-openentry.md), [IMAPIContainer::OpenEntry](imapicontainer-openentry.md), [IMAPISession::OpenEntry](imapisession-openentry.md), [IMAPISupport::OpenEntry](imapisupport-openentry.md), [IMsgStore::OpenEntry](imsgstore-openentry.md), [IMSLogon::OpenEntry](imslogon-openentry.md)</span></span>
    
- <span data-ttu-id="2b737-157">Uma \*\*\*\* estrutura ENTRYID é usada para armazenar um identificador de entrada no disco.</span><span class="sxs-lookup"><span data-stu-id="2b737-157">An **ENTRYID** structure is used to store an entry identifier on disk.</span></span> <span data-ttu-id="2b737-158">Uma estrutura **FLATENTRY** é usada para armazenar um identificador de entrada em um arquivo ou passá-lo em um fluxo de bytes.</span><span class="sxs-lookup"><span data-stu-id="2b737-158">A **FLATENTRY** structure is used to store an entry identifier in a file or pass it in a stream of bytes.</span></span> 
    
<span data-ttu-id="2b737-159">Os clientes devem sempre passar por identificadores de entrada alinhados naturalmente.</span><span class="sxs-lookup"><span data-stu-id="2b737-159">Clients should always pass in naturally aligned entry identifiers.</span></span> <span data-ttu-id="2b737-160">Embora os provedores manipulem identificadores de entrada com alinhamento arbitrária, os clientes não devem esperar esse comportamento.</span><span class="sxs-lookup"><span data-stu-id="2b737-160">Although providers should handle arbitrarily aligned entry identifiers, clients should not expect this behavior.</span></span> <span data-ttu-id="2b737-161">A falha ao passar um identificador de entrada alinhada para um método pode causar uma falha de alinhamento nos processadores RISC.</span><span class="sxs-lookup"><span data-stu-id="2b737-161">Failure to pass a good aligned entry identifier to a method can cause an alignment fault on RISC processors.</span></span> 
  
<span data-ttu-id="2b737-162">O fator de alinhamento natural, geralmente 8 bytes, é o maior tipo de dados suportado pela CPU e, normalmente, o mesmo fator de alinhamento usado pelo alocador de memória do sistema.</span><span class="sxs-lookup"><span data-stu-id="2b737-162">The natural alignment factor, typically 8 bytes, is the largest data type supported by the CPU, and usually the same alignment factor used by the system memory allocator.</span></span> <span data-ttu-id="2b737-163">Um endereço de memória logicamente alinhado permite que a CPU acesse qualquer tipo de dados compatível com esse endereço sem gerar uma falha de alinhamento.</span><span class="sxs-lookup"><span data-stu-id="2b737-163">A naturally aligned memory address allows the CPU to access any data type it supports at that address without generating an alignment fault.</span></span> <span data-ttu-id="2b737-164">Para CPUs RISC, um tipo de dados de tamanho N bytes geralmente deve ser alinhado em um múltiplo par de N bytes, sendo que o endereço é um múltiplo de N.</span><span class="sxs-lookup"><span data-stu-id="2b737-164">For RISC CPUs, a data type of size N bytes must usually be aligned on an even multiple of N bytes, with the address being an even multiple of N.</span></span>
  
<span data-ttu-id="2b737-165">Para obter mais informações, consulte identificadores de [entrada](mapi-entry-identifiers.md).</span><span class="sxs-lookup"><span data-stu-id="2b737-165">For more information, see [Entry Identifiers](mapi-entry-identifiers.md).</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="2b737-166">Confira também</span><span class="sxs-lookup"><span data-stu-id="2b737-166">See also</span></span>



[<span data-ttu-id="2b737-167">FLATENTRY</span><span class="sxs-lookup"><span data-stu-id="2b737-167">FLATENTRY</span></span>](flatentry.md)
  
[<span data-ttu-id="2b737-168">IMAPISupport::CompareEntryIDs</span><span class="sxs-lookup"><span data-stu-id="2b737-168">IMAPISupport::CompareEntryIDs</span></span>](imapisupport-compareentryids.md)
  
[<span data-ttu-id="2b737-169">Propriedade canônica PidTagRecordKey</span><span class="sxs-lookup"><span data-stu-id="2b737-169">PidTagRecordKey Canonical Property</span></span>](pidtagrecordkey-canonical-property.md)


[<span data-ttu-id="2b737-170">Estruturas MAPI</span><span class="sxs-lookup"><span data-stu-id="2b737-170">MAPI Structures</span></span>](mapi-structures.md)

