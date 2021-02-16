---
title: NSTServiceEntry
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 5ada6363-2406-4c0a-8326-a299a8bbefe1
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: 96c04a242c477204ea1447fb78c31d189eeac59a
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32280051"
---
# <a name="nstserviceentry"></a><span data-ttu-id="fbeda-103">NSTServiceEntry</span><span class="sxs-lookup"><span data-stu-id="fbeda-103">NSTServiceEntry</span></span>

  
  
<span data-ttu-id="fbeda-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="fbeda-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="fbeda-105">Função de ponto de entrada do serviço de mensagens para um provedor de armazenamento MAPI quebrar um armazenamento local baseado em PST como um armazenamento NST.</span><span class="sxs-lookup"><span data-stu-id="fbeda-105">Message service entry point function for a MAPI store provider to wrap a PST-based local store as an NST store.</span></span> 
  
## <a name="quick-info"></a><span data-ttu-id="fbeda-106">Informações rápidas</span><span class="sxs-lookup"><span data-stu-id="fbeda-106">Quick info</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="fbeda-107">Implementado por:</span><span class="sxs-lookup"><span data-stu-id="fbeda-107">Implemented by:</span></span>  <br/> |<span data-ttu-id="fbeda-108">Provedor MAPI</span><span class="sxs-lookup"><span data-stu-id="fbeda-108">MAPI provider</span></span>  <br/> |
|<span data-ttu-id="fbeda-109">Chamado por:</span><span class="sxs-lookup"><span data-stu-id="fbeda-109">Called by:</span></span>  <br/> |<span data-ttu-id="fbeda-110">MAPI</span><span class="sxs-lookup"><span data-stu-id="fbeda-110">MAPI</span></span>  <br/> |
   
```cpp
HRESULT NSTServiceEntry( 
    HINSTANCE hInstance,   
    LPMALLOC lpMalloc, 
    LPMAPISUP lpMAPISup, 
    ULONG ulUIParam, 
    ULONG ulFlags, 
    ULONG ulContext, 
    ULONG cValues, 
    LPSPropValue lpProps, 
    LPPROVIDERADMIN lpProviderAdmin, 
    LPMAPIERROR FAR * lppMapiError 
);
```

## <a name="parameters"></a><span data-ttu-id="fbeda-111">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="fbeda-111">Parameters</span></span>

 <span data-ttu-id="fbeda-112">**NSTServiceEntry** usa o protótipo **[de função MSGSERVICEENTRY.](msgserviceentry.md)**</span><span class="sxs-lookup"><span data-stu-id="fbeda-112">**NSTServiceEntry** uses the **[MSGSERVICEENTRY](msgserviceentry.md)** function prototype.</span></span> <span data-ttu-id="fbeda-113">Para obter informações sobre seus parâmetros, consulte **[MSGSERVICEENTRY](msgserviceentry.md)**.</span><span class="sxs-lookup"><span data-stu-id="fbeda-113">For information on its parameters, see **[MSGSERVICEENTRY](msgserviceentry.md)**.</span></span> 
  
## <a name="return-values"></a><span data-ttu-id="fbeda-114">Valor de retorno</span><span class="sxs-lookup"><span data-stu-id="fbeda-114">Return values</span></span>

<span data-ttu-id="fbeda-115">Para obter informações sobre valores de retorno, consulte **[MSGSERVICEENTRY](msgserviceentry.md)**.</span><span class="sxs-lookup"><span data-stu-id="fbeda-115">For information on return values, see **[MSGSERVICEENTRY](msgserviceentry.md)**.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="fbeda-116">Comentários</span><span class="sxs-lookup"><span data-stu-id="fbeda-116">Remarks</span></span>

<span data-ttu-id="fbeda-117">Ao usar **[GetProcAddress](https://msdn.microsoft.com/library/ms683212.aspx)** para procurar o endereço dessa função no msmapi32.dll, especifique "NSTServiceEntry" como o nome do procedimento.</span><span class="sxs-lookup"><span data-stu-id="fbeda-117">When using **[GetProcAddress](https://msdn.microsoft.com/library/ms683212.aspx)** to look for the address of this function in msmapi32.dll, specify "NSTServiceEntry" as the procedure name.</span></span> 
  
<span data-ttu-id="fbeda-118">Para usar a API de replicação, um provedor de armazenamento MAPI deve primeiro abrir e quebrar um armazenamento local baseado em PST chamando **[NSTServiceEntry](nstserviceentry.md)**.</span><span class="sxs-lookup"><span data-stu-id="fbeda-118">To use the Replication API, a MAPI store provider must first open and wrap a PST-based local store by calling **[NSTServiceEntry](nstserviceentry.md)**.</span></span> <span data-ttu-id="fbeda-119">Em seguida, o provedor pode usar as principais interfaces da API, **[IOSTX](iostxiunknown.md)** e **[IPSTX](ipstxiunknown.md)** para realizar a replicação.</span><span class="sxs-lookup"><span data-stu-id="fbeda-119">The provider can then use the major interfaces of the API, **[IOSTX](iostxiunknown.md)** and **[IPSTX](ipstxiunknown.md)**, to carry out replication.</span></span> 
  
<span data-ttu-id="fbeda-120">Os comentários a seguir se aplicam a um armazenamento NST:</span><span class="sxs-lookup"><span data-stu-id="fbeda-120">The following remarks apply to an NST store:</span></span>
  
- <span data-ttu-id="fbeda-121">Não armazene nenhuma informação na seção de perfil global ao implementar um provedor MAPI que usa **NSTServiceEntry**.</span><span class="sxs-lookup"><span data-stu-id="fbeda-121">Do not store any information in the global profile section when implementing a MAPI provider that uses **NSTServiceEntry**.</span></span> <span data-ttu-id="fbeda-122">A seção de perfil global é compartilhada por muitos provedores e os dados armazenados nesse perfil podem ser substituídos.</span><span class="sxs-lookup"><span data-stu-id="fbeda-122">The global profile section is shared by many providers and data stored in this profile can be overwritten.</span></span> 
    
- <span data-ttu-id="fbeda-123">Somente os itens com carimbos de data/hora de modificação existentes têm seus carimbos atualizados quando são salvos.</span><span class="sxs-lookup"><span data-stu-id="fbeda-123">Only items with existing modification time stamps get their stamps updated when they are saved.</span></span> 
    
- <span data-ttu-id="fbeda-124">A verificação de conflitos não ocorre automaticamente quando os itens são salvos.</span><span class="sxs-lookup"><span data-stu-id="fbeda-124">Conflict-checking does not occur automatically when items are saved.</span></span>
    
-  <span data-ttu-id="fbeda-125">A detecção duplicada não ocorre quando os itens são salvos.</span><span class="sxs-lookup"><span data-stu-id="fbeda-125">Duplicate detection does not occur when items are saved.</span></span> 
    
-  <span data-ttu-id="fbeda-126">O arquivo que representa a versão em cache do servidor é anexado a . NST.</span><span class="sxs-lookup"><span data-stu-id="fbeda-126">The file representing the cached version of the server is appended with .NST.</span></span> 
    
- <span data-ttu-id="fbeda-127">Para obter um ponteiro para a seção de perfil global, um serviço de mensagens chama **[IMAPISupport::OpenProfileSection](imapisupport-openprofilesection.md)** no objeto de suporte usando **pbNSTGlobalProfileSectionGuid** conforme definido abaixo:</span><span class="sxs-lookup"><span data-stu-id="fbeda-127">To obtain a pointer to the global profile section, a message service calls **[IMAPISupport::OpenProfileSection](imapisupport-openprofilesection.md)** in the support object using **pbNSTGlobalProfileSectionGuid** as defined below:</span></span> 
    
  ```
  #define  pbNSTGlobalProfileSectionGuid "\x85\xED\x14\x23\x9D\xF7\x42\x66\x8B\xF2\xFB\xD4\xA5\x21\x29\x41"
  ```

- <span data-ttu-id="fbeda-128">Nesse caso, o objeto de suporte do serviço de mensagens deve garantir que **IMAPISupport::OpenProfileSection** retorne a seção de perfil identificada pela propriedade **[PR_SERVICE_UID](pidtagserviceuid-canonical-property.md)** na seção de perfil padrão.</span><span class="sxs-lookup"><span data-stu-id="fbeda-128">In this case, the support object of the message service should ensure that **IMAPISupport::OpenProfileSection** returns the profile section that is identified by the **[PR_SERVICE_UID](pidtagserviceuid-canonical-property.md)** property in the default profile section.</span></span> <span data-ttu-id="fbeda-129">Para obter esta seção de perfil, o objeto de suporte pode abrir a seção de perfil padrão, recuperar **PR_SERVICE_UID** e passar o resultado para **IMAPISupport::OpenProfileSection** para recuperar a seção de perfil global correta.</span><span class="sxs-lookup"><span data-stu-id="fbeda-129">To get this profile section, the support object can open the default profile section, retrieve **PR_SERVICE_UID**, and pass the result to **IMAPISupport::OpenProfileSection** to retrieve the correct global profile section.</span></span> <span data-ttu-id="fbeda-130">O objeto de suporte, por sua vez, retorna um ponteiro para essa seção de perfil global para o serviço de mensagens.</span><span class="sxs-lookup"><span data-stu-id="fbeda-130">The support object in turn returns a pointer to this global profile section to the message service.</span></span> 
    
## <a name="see-also"></a><span data-ttu-id="fbeda-131">Confira também</span><span class="sxs-lookup"><span data-stu-id="fbeda-131">See also</span></span>



[<span data-ttu-id="fbeda-132">Sobre a API de replicação</span><span class="sxs-lookup"><span data-stu-id="fbeda-132">About the Replication API</span></span>](about-the-replication-api.md)

