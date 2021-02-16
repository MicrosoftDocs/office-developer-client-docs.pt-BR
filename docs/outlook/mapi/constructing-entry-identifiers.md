---
title: Construindo identificadores de entrada
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: bc2a9116-948e-4da3-96b8-26d73bcd63c4
description: 'Última modificação: 23 de julho de 2011'
ms.openlocfilehash: 8d48c2584fa5b7e862102e401ea8165821607f77
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33427945"
---
# <a name="constructing-entry-identifiers"></a><span data-ttu-id="dec5b-103">Construindo identificadores de entrada</span><span class="sxs-lookup"><span data-stu-id="dec5b-103">Constructing Entry Identifiers</span></span>

  
  
<span data-ttu-id="dec5b-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="dec5b-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="dec5b-105">Os identificadores de entrada são construídos com a [estrutura ENTRYID.](entryid.md)</span><span class="sxs-lookup"><span data-stu-id="dec5b-105">Entry identifiers are constructed with the [ENTRYID](entryid.md) structure.</span></span> <span data-ttu-id="dec5b-106">A **estrutura ENTRYID** é composta por um sinalizador que descreve os atributos do identificador de entrada e o identificador de entrada real.</span><span class="sxs-lookup"><span data-stu-id="dec5b-106">The **ENTRYID** structure is composed of a flag that describes the attributes of the entry identifier and the actual entry identifier.</span></span> 
  
## <a name="entryid-structure"></a><span data-ttu-id="dec5b-107">Estrutura ENTRYID</span><span class="sxs-lookup"><span data-stu-id="dec5b-107">ENTRYID Structure</span></span>

<span data-ttu-id="dec5b-108">A **estrutura ENTRYID** é definida da seguinte forma:</span><span class="sxs-lookup"><span data-stu-id="dec5b-108">The **ENTRYID** structure is defined as follows:</span></span> 
  
```cpp
typedef struct
{
    BYTE        abFlags[4];
    BYTE        ab[MAPI_DIM];
}  ENTRYID, FAR *LPENTRYID;
 
```

<span data-ttu-id="dec5b-109">MAPI_DIM é uma constante definida no arquivo de header MapiDefs.h.</span><span class="sxs-lookup"><span data-stu-id="dec5b-109">MAPI_DIM is a constant that is defined in the MapiDefs.h header file.</span></span> 
  
<span data-ttu-id="dec5b-110">O primeiro byte do membro **abFlags** de 4 byte descreve o tipo e o uso do identificador de entrada e pode ter os seguintes valores:</span><span class="sxs-lookup"><span data-stu-id="dec5b-110">The first byte of the 4-byte **abFlags** member describes the type and use of the entry identifier and can have the following values:</span></span> 
  
- <span data-ttu-id="dec5b-111">MAPI_NOTRECI — Indica que o identificador de entrada não pode ser usado como um destinatário em uma mensagem.</span><span class="sxs-lookup"><span data-stu-id="dec5b-111">MAPI_NOTRECI — Indicates the entry identifier cannot be used as a recipient on a message.</span></span>
    
- <span data-ttu-id="dec5b-112">MAPI_NOTRESERVED — Indica que outros usuários não podem acessar o identificador de entrada.</span><span class="sxs-lookup"><span data-stu-id="dec5b-112">MAPI_NOTRESERVED — Indicates that other users cannot access the entry identifier.</span></span>
    
- <span data-ttu-id="dec5b-113">MAPI_NOW — Indica que o identificador de entrada não pode ser usado em outras ocasiões.</span><span class="sxs-lookup"><span data-stu-id="dec5b-113">MAPI_NOW — Indicates that the entry identifier cannot be used at other times.</span></span>
    
- <span data-ttu-id="dec5b-114">MAPI_SHORTTERM — Indica que o identificador de entrada é de curto prazo.</span><span class="sxs-lookup"><span data-stu-id="dec5b-114">MAPI_SHORTTERM — Indicates that the entry identifier is short-term.</span></span> <span data-ttu-id="dec5b-115">Todos os outros valores nesse byte devem ser definidos, a menos que outros usos do identificador de entrada sejam permitidos.</span><span class="sxs-lookup"><span data-stu-id="dec5b-115">All other values in this byte must be set unless other uses of the entry identifier are allowed.</span></span>
    
- <span data-ttu-id="dec5b-116">MAPI_THISSESSION — Indica que o identificador de entrada não pode ser usado em outras sessões.</span><span class="sxs-lookup"><span data-stu-id="dec5b-116">MAPI_THISSESSION — Indicates that the entry identifier cannot be used on other sessions.</span></span>
    
- <span data-ttu-id="dec5b-117">MAPI_NOTRESERVED — Indica que o identificador de entrada pode ser usado por outros provedores de serviços para outros objetos.</span><span class="sxs-lookup"><span data-stu-id="dec5b-117">MAPI_NOTRESERVED — Indicates that the entry identifier can be used by other service providers for other objects.</span></span>
    
<span data-ttu-id="dec5b-118">O **ab** member of entry identifiers that is created by address book and message store providers is composed of two pieces: a 16-byte [MAPIUID](mapiuid.md) structure that identifies the service provider, and a piece to identify the object.</span><span class="sxs-lookup"><span data-stu-id="dec5b-118">The **ab** member of entry identifiers that is created by address book and message store providers is composed of two pieces: a 16-byte [MAPIUID](mapiuid.md) structure that identifies the service provider, and a piece to identify the object.</span></span> <span data-ttu-id="dec5b-119">**MAPIUID** é uma estrutura que contém um identificador global exclusivo, ou GUID.</span><span class="sxs-lookup"><span data-stu-id="dec5b-119">**MAPIUID** is a structure that contains a globally unique identifier, or GUID.</span></span> <span data-ttu-id="dec5b-120">Um GUID é um identificador independente de ordem de byte que pode ser criado usando a ferramenta Criar *GUID*\* do Microsoft Visual Studio.</span><span class="sxs-lookup"><span data-stu-id="dec5b-120">A GUID is a byte-order-independent identifier that can be created by using the Microsoft Visual Studio *Create GUID*\* tool.</span></span> 
  
<span data-ttu-id="dec5b-121">Um provedor de serviços registra sua estrutura **MAPIUID** com MAPI durante o processo de logon em uma chamada para o método [IMAPISupport::SetProviderUID.](imapisupport-setprovideruid.md)</span><span class="sxs-lookup"><span data-stu-id="dec5b-121">A service provider registers its **MAPIUID** structure with MAPI during the logon process in a call to the [IMAPISupport::SetProviderUID](imapisupport-setprovideruid.md) method.</span></span> <span data-ttu-id="dec5b-122">Quando um cliente chama um **método OpenEntry** para acessar um objeto, o MAPI usa a estrutura **MAPIUID** para determinar qual provedor de serviços pode fornecer esse acesso.</span><span class="sxs-lookup"><span data-stu-id="dec5b-122">When a client calls an **OpenEntry** method to access an object, MAPI uses the **MAPIUID** structure to determine which service provider can provide that access.</span></span> <span data-ttu-id="dec5b-123">Os provedores de serviços devem usar a mesma **estrutura MAPIUID** para todas as versões de sua DLL.</span><span class="sxs-lookup"><span data-stu-id="dec5b-123">Service providers should use the same **MAPIUID** structure for all versions of their DLL.</span></span> <span data-ttu-id="dec5b-124">Isso permite que os clientes com a versão mais recente respondam a mensagens enviadas e salvas com a versão mais antiga.</span><span class="sxs-lookup"><span data-stu-id="dec5b-124">This enables clients with the newer version to respond to messages sent and saved with the older version.</span></span> 
  
<span data-ttu-id="dec5b-125">O restante do membro **ab** após o **MAPIUID** de 16 byte contém dados binários específicos do provedor de serviços para identificar objetos específicos.</span><span class="sxs-lookup"><span data-stu-id="dec5b-125">The rest of the **ab** member after the 16-byte **MAPIUID** contains service-provider-specific binary data for identifying particular objects.</span></span> <span data-ttu-id="dec5b-126">Não há nenhum tamanho fixo para essa parte do identificador de entrada.</span><span class="sxs-lookup"><span data-stu-id="dec5b-126">There is no fixed size for this portion of the entry identifier.</span></span> <span data-ttu-id="dec5b-127">Pode ser de qualquer tamanho, dentro do motivo.</span><span class="sxs-lookup"><span data-stu-id="dec5b-127">It can be any size, within reason.</span></span> <span data-ttu-id="dec5b-128">Um provedor de serviços normalmente inclui as seguintes informações nesta parte de seus identificadores de entrada:</span><span class="sxs-lookup"><span data-stu-id="dec5b-128">A service provider typically includes the following information in this part of its entry identifiers:</span></span> 
  
- <span data-ttu-id="dec5b-129">Informações de versão — Como é comum para um provedor de serviços alterar o formato de seus identificadores de entrada de versão para versão, o armazenamento de informações de versão possibilita determinar rapidamente como descobrir qualquer identificador de entrada.</span><span class="sxs-lookup"><span data-stu-id="dec5b-129">Version information — Because it is common for a service provider to change the format of its entry identifiers from version to version, storing version information makes it possible to quickly determine how to decipher any entry identifier.</span></span>
    
- <span data-ttu-id="dec5b-130">Informações de local — As informações de local são dados que dão a um provedor de serviços um indicador de como localizar o objeto representado pelo identificador de entrada.</span><span class="sxs-lookup"><span data-stu-id="dec5b-130">Location information — Location information is data that gives a service provider an indicator of how to locate the object represented by the entry identifier.</span></span> <span data-ttu-id="dec5b-131">Por exemplo, um provedor de serviços pode armazenar o deslocamento de disco para o último local em um arquivo de dados em que o objeto foi armazenado.</span><span class="sxs-lookup"><span data-stu-id="dec5b-131">For example, a service provider can store the disk offset for the last place in a data file that the object was stored.</span></span> <span data-ttu-id="dec5b-132">Como esse tipo de informação pode mudar ao longo do tempo, os provedores de serviços devem fornecer várias maneiras de localizar objetos em seus identificadores de entrada.</span><span class="sxs-lookup"><span data-stu-id="dec5b-132">Because this type of information can change over time, service providers should provide multiple ways for locating objects in their entry identifiers.</span></span>
    
<span data-ttu-id="dec5b-133">Embora os provedores de serviços possam reciclar seus identificadores de entrada, eles devem evitar essa prática.</span><span class="sxs-lookup"><span data-stu-id="dec5b-133">Although service providers can recycle their entry identifiers, they should avoid this practice.</span></span> <span data-ttu-id="dec5b-134">Se for necessário reutilizar um identificador de entrada, os provedores de serviços deverão tornar o período de tempo que se desdoba entre o uso inicial e a reutilização o máximo possível.</span><span class="sxs-lookup"><span data-stu-id="dec5b-134">If it is necessary to reuse an entry identifier, service providers should make the time period that elapses between the initial use and the reuse as long as possible.</span></span> <span data-ttu-id="dec5b-135">Além disso, o identificador de entrada deve ser reatribuido a outro objeto do mesmo tipo.</span><span class="sxs-lookup"><span data-stu-id="dec5b-135">Also, the entry identifier should be reassigned to another object of the same type.</span></span> <span data-ttu-id="dec5b-136">Ou seja, um identificador de entrada específico não deve ser associado primeiro a uma mensagem e, em seguida, a uma pasta.</span><span class="sxs-lookup"><span data-stu-id="dec5b-136">That is, a particular entry identifier should not be associated first with a message and then with a folder.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="dec5b-137">Confira também</span><span class="sxs-lookup"><span data-stu-id="dec5b-137">See also</span></span>



[<span data-ttu-id="dec5b-138">Identificadores de entrada MAPI</span><span class="sxs-lookup"><span data-stu-id="dec5b-138">MAPI Entry Identifiers</span></span>](mapi-entry-identifiers.md)

