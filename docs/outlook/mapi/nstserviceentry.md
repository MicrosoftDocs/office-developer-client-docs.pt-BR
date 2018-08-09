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
ms.openlocfilehash: b5902c25197c2ae5790e654a8f29227e107b4a72
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19768158"
---
# <a name="nstserviceentry"></a><span data-ttu-id="1b590-103">NSTServiceEntry</span><span class="sxs-lookup"><span data-stu-id="1b590-103">NSTServiceEntry</span></span>

  
  
<span data-ttu-id="1b590-104">**Aplica-se a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="1b590-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="1b590-105">Função de ponto de entrada de serviço de mensagem para um MAPI armazenar provedor para empacotar um repositório local baseado em PST como um repositório NST.</span><span class="sxs-lookup"><span data-stu-id="1b590-105">Message service entry point function for a MAPI store provider to wrap a PST-based local store as an NST store.</span></span> 
  
## <a name="quick-info"></a><span data-ttu-id="1b590-106">Informações rápidas</span><span class="sxs-lookup"><span data-stu-id="1b590-106">Quick info</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="1b590-107">Implementada por:</span><span class="sxs-lookup"><span data-stu-id="1b590-107">Implemented by:</span></span>  <br/> |<span data-ttu-id="1b590-108">Provedor MAPI</span><span class="sxs-lookup"><span data-stu-id="1b590-108">MAPI provider</span></span>  <br/> |
|<span data-ttu-id="1b590-109">Chamado pelo:</span><span class="sxs-lookup"><span data-stu-id="1b590-109">Called by:</span></span>  <br/> |<span data-ttu-id="1b590-110">MAPI</span><span class="sxs-lookup"><span data-stu-id="1b590-110">MAPI</span></span>  <br/> |
   
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

## <a name="parameters"></a><span data-ttu-id="1b590-111">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="1b590-111">Parameters</span></span>

 <span data-ttu-id="1b590-112">**NSTServiceEntry** usa o protótipo de função **[MSGSERVICEENTRY](msgserviceentry.md)** .</span><span class="sxs-lookup"><span data-stu-id="1b590-112">**NSTServiceEntry** uses the **[MSGSERVICEENTRY](msgserviceentry.md)** function prototype.</span></span> <span data-ttu-id="1b590-113">Para obter informações sobre seus parâmetros, consulte **[MSGSERVICEENTRY](msgserviceentry.md)**.</span><span class="sxs-lookup"><span data-stu-id="1b590-113">For information on its parameters, see **[MSGSERVICEENTRY](msgserviceentry.md)**.</span></span> 
  
## <a name="return-values"></a><span data-ttu-id="1b590-114">Valores de retorno</span><span class="sxs-lookup"><span data-stu-id="1b590-114">Return values</span></span>

<span data-ttu-id="1b590-115">Para obter informações sobre valores de retorno, consulte **[MSGSERVICEENTRY](msgserviceentry.md)**.</span><span class="sxs-lookup"><span data-stu-id="1b590-115">For information on return values, see **[MSGSERVICEENTRY](msgserviceentry.md)**.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="1b590-116">Comentários</span><span class="sxs-lookup"><span data-stu-id="1b590-116">Remarks</span></span>

<span data-ttu-id="1b590-117">Ao usar o **[GetProcAddress](http://msdn.microsoft.com/en-us/library/ms683212.aspx)** para procurar o endereço desta função no Msmapi32, especifique "NSTServiceEntry" como o nome do procedimento.</span><span class="sxs-lookup"><span data-stu-id="1b590-117">When using **[GetProcAddress](http://msdn.microsoft.com/en-us/library/ms683212.aspx)** to look for the address of this function in msmapi32.dll, specify "NSTServiceEntry" as the procedure name.</span></span> 
  
<span data-ttu-id="1b590-118">Para usar a API de replicação, um provedor de repositório MAPI deve primeiro abrir e quebrar um repositório local baseado em PST chamando **[NSTServiceEntry](nstserviceentry.md)**.</span><span class="sxs-lookup"><span data-stu-id="1b590-118">To use the Replication API, a MAPI store provider must first open and wrap a PST-based local store by calling **[NSTServiceEntry](nstserviceentry.md)**.</span></span> <span data-ttu-id="1b590-119">O provedor, em seguida, pode usar as interfaces principais da API, **[IOSTX](iostxiunknown.md)** e **[IPSTX](ipstxiunknown.md)**, para realizar a replicação.</span><span class="sxs-lookup"><span data-stu-id="1b590-119">The provider can then use the major interfaces of the API, **[IOSTX](iostxiunknown.md)** and **[IPSTX](ipstxiunknown.md)**, to carry out replication.</span></span> 
  
<span data-ttu-id="1b590-120">Os comentários a seguir se aplicam a um repositório NST:</span><span class="sxs-lookup"><span data-stu-id="1b590-120">The following remarks apply to an NST store:</span></span>
  
- <span data-ttu-id="1b590-121">Não armazene qualquer informação na seção perfil global ao implementar um provedor MAPI que usa **NSTServiceEntry**.</span><span class="sxs-lookup"><span data-stu-id="1b590-121">Do not store any information in the global profile section when implementing a MAPI provider that uses **NSTServiceEntry**.</span></span> <span data-ttu-id="1b590-122">A seção perfil global é compartilhada por vários provedores e dados armazenados neste perfil podem ser substituídos.</span><span class="sxs-lookup"><span data-stu-id="1b590-122">The global profile section is shared by many providers and data stored in this profile can be overwritten.</span></span> 
    
- <span data-ttu-id="1b590-123">Somente os itens cujo existente carimbos de hora de modificação obtém seus carimbos atualizados quando elas forem salvas.</span><span class="sxs-lookup"><span data-stu-id="1b590-123">Only items with existing modification time stamps get their stamps updated when they are saved.</span></span> 
    
- <span data-ttu-id="1b590-124">Verificação de conflito não ocorre automaticamente quando itens são salvos.</span><span class="sxs-lookup"><span data-stu-id="1b590-124">Conflict-checking does not occur automatically when items are saved.</span></span>
    
-  <span data-ttu-id="1b590-125">Detecção de duplicatas não ocorrerá quando os itens são salvos.</span><span class="sxs-lookup"><span data-stu-id="1b590-125">Duplicate detection does not occur when items are saved.</span></span> 
    
-  <span data-ttu-id="1b590-126">O arquivo que representa a versão em cache do servidor é acrescentado com. NST.</span><span class="sxs-lookup"><span data-stu-id="1b590-126">The file representing the cached version of the server is appended with .NST.</span></span> 
    
- <span data-ttu-id="1b590-127">Para obter um ponteiro para a seção perfil global, um serviço de mensagem chama **[IMAPISupport::OpenProfileSection](imapisupport-openprofilesection.md)** no objeto suporte usando **pbNSTGlobalProfileSectionGuid** , conforme definido abaixo:</span><span class="sxs-lookup"><span data-stu-id="1b590-127">To obtain a pointer to the global profile section, a message service calls **[IMAPISupport::OpenProfileSection](imapisupport-openprofilesection.md)** in the support object using **pbNSTGlobalProfileSectionGuid** as defined below:</span></span> 
    
  ```
  #define  pbNSTGlobalProfileSectionGuid "\x85\xED\x14\x23\x9D\xF7\x42\x66\x8B\xF2\xFB\xD4\xA5\x21\x29\x41"
  ```

- <span data-ttu-id="1b590-128">Nesse caso, o objeto de suporte do serviço de mensagem deve assegurar que **IMAPISupport::OpenProfileSection** retorna a seção de perfil que é identificada pela propriedade **[PR_SERVICE_UID](pidtagserviceuid-canonical-property.md)** na seção perfil padrão.</span><span class="sxs-lookup"><span data-stu-id="1b590-128">In this case, the support object of the message service should ensure that **IMAPISupport::OpenProfileSection** returns the profile section that is identified by the **[PR_SERVICE_UID](pidtagserviceuid-canonical-property.md)** property in the default profile section.</span></span> <span data-ttu-id="1b590-129">Para fazer esta seção de perfil, o objeto de suporte pode abrir a seção de perfil padrão, recuperar **PR_SERVICE_UID**e passar o resultado para **IMAPISupport::OpenProfileSection** para recuperar a seção de perfil global correto.</span><span class="sxs-lookup"><span data-stu-id="1b590-129">To get this profile section, the support object can open the default profile section, retrieve **PR_SERVICE_UID**, and pass the result to **IMAPISupport::OpenProfileSection** to retrieve the correct global profile section.</span></span> <span data-ttu-id="1b590-130">Por sua vez, o objeto de suporte retorna um ponteiro para esta seção perfil global para o serviço de mensagem.</span><span class="sxs-lookup"><span data-stu-id="1b590-130">The support object in turn returns a pointer to this global profile section to the message service.</span></span> 
    
## <a name="see-also"></a><span data-ttu-id="1b590-131">Confira também</span><span class="sxs-lookup"><span data-stu-id="1b590-131">See also</span></span>



[<span data-ttu-id="1b590-132">Sobre a API de replicação</span><span class="sxs-lookup"><span data-stu-id="1b590-132">About the Replication API</span></span>](about-the-replication-api.md)

