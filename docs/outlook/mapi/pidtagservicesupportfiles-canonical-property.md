---
title: Propriedade canônica PidTagServiceSupportFiles
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagServiceSupportFiles
api_type:
- COM
ms.assetid: df4be986-62a8-49d6-8eca-25b55c74f830
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: 2dc431d807bd74640e5b5a9c020f668b13530197
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19770060"
---
# <a name="pidtagservicesupportfiles-canonical-property"></a><span data-ttu-id="d0da3-103">Propriedade canônica PidTagServiceSupportFiles</span><span class="sxs-lookup"><span data-stu-id="d0da3-103">PidTagServiceSupportFiles Canonical Property</span></span>

  
  
<span data-ttu-id="d0da3-104">**Aplica-se a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="d0da3-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="d0da3-105">Contém uma lista dos arquivos que pertencem ao serviço de mensagem.</span><span class="sxs-lookup"><span data-stu-id="d0da3-105">Contains a list of the files that belong to the message service.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="d0da3-106">Propriedades associadas:</span><span class="sxs-lookup"><span data-stu-id="d0da3-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="d0da3-107">PR_SERVICE_SUPPORT_FILES, PR_SERVICE_SUPPORT_FILES_A, PR_SERVICE_SUPPORT_FILES_W</span><span class="sxs-lookup"><span data-stu-id="d0da3-107">PR_SERVICE_SUPPORT_FILES, PR_SERVICE_SUPPORT_FILES_A, PR_SERVICE_SUPPORT_FILES_W</span></span>  <br/> |
|<span data-ttu-id="d0da3-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="d0da3-108">Identifier:</span></span>  <br/> |<span data-ttu-id="d0da3-109">0x3D0F</span><span class="sxs-lookup"><span data-stu-id="d0da3-109">0x3D0F</span></span>  <br/> |
|<span data-ttu-id="d0da3-110">Tipo de dados:</span><span class="sxs-lookup"><span data-stu-id="d0da3-110">Data type:</span></span>  <br/> |<span data-ttu-id="d0da3-111">PT_MV_STRING8, PT_MV_UNICODE</span><span class="sxs-lookup"><span data-stu-id="d0da3-111">PT_MV_STRING8, PT_MV_UNICODE</span></span>  <br/> |
|<span data-ttu-id="d0da3-112">Área:</span><span class="sxs-lookup"><span data-stu-id="d0da3-112">Area:</span></span>  <br/> |<span data-ttu-id="d0da3-113">Perfil MAPI</span><span class="sxs-lookup"><span data-stu-id="d0da3-113">MAPI profile</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="d0da3-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="d0da3-114">Remarks</span></span>

<span data-ttu-id="d0da3-115">Usando uma caixa de diálogo no miniaplicativo do painel de controle, um usuário pode obter a lista de arquivos que pertencem ao serviço de mensagem.</span><span class="sxs-lookup"><span data-stu-id="d0da3-115">Using a dialog box in the control panel applet, a user can obtain the list of files that belong to the message service.</span></span> <span data-ttu-id="d0da3-116">Por exemplo, o usuário pode obter os nomes de todas as bibliotecas de vínculos dinâmicos (DLLs) que pertencem ao serviço.</span><span class="sxs-lookup"><span data-stu-id="d0da3-116">For example, the user can obtain the names of all dynamic-link libraries (DLLs) that belong to the service.</span></span> <span data-ttu-id="d0da3-117">O usuário pode então seek detalhes adicionais sobre os arquivos especificados, como os nomes e números de versão de todas as DLLs.</span><span class="sxs-lookup"><span data-stu-id="d0da3-117">The user can then seek additional details about the specified files, such as the names and version numbers of all the DLLs.</span></span> <span data-ttu-id="d0da3-118">O MAPI usa a essas propriedades para criar uma lista de arquivos de suporte em uma caixa de diálogo para seleção de usuário de mensagens.</span><span class="sxs-lookup"><span data-stu-id="d0da3-118">MAPI uses the these properties to create a support file list in a dialog box for messaging user selection.</span></span>
  
<span data-ttu-id="d0da3-119">MAPI funciona somente com nomes de arquivo e outras cadeias de caracteres passada para ele, no conjunto de caracteres do Active Directory Service Interfaces (ANSI).</span><span class="sxs-lookup"><span data-stu-id="d0da3-119">MAPI works only with filenames, and other strings passed to it, in the Active Directory Service Interfaces (ANSI) character set.</span></span> <span data-ttu-id="d0da3-120">Aplicativos cliente que usam nomes de arquivo em um conjunto de caracteres do fabricante do equipamento original (OEM) devem convertê-los para ANSI antes de chamar MAPI.</span><span class="sxs-lookup"><span data-stu-id="d0da3-120">Client applications that use filenames in an original equipment manufacturer (OEM) character set must convert them to ANSI before calling MAPI.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="d0da3-121">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="d0da3-121">Related resources</span></span>

### <a name="header-files"></a><span data-ttu-id="d0da3-122">Arquivos de cabeçalho</span><span class="sxs-lookup"><span data-stu-id="d0da3-122">Header files</span></span>

<span data-ttu-id="d0da3-123">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="d0da3-123">Mapidefs.h</span></span>
  
> <span data-ttu-id="d0da3-124">Fornece definições de tipo de dados.</span><span class="sxs-lookup"><span data-stu-id="d0da3-124">Provides data type definitions.</span></span>
    
<span data-ttu-id="d0da3-125">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="d0da3-125">Mapitags.h</span></span>
  
> <span data-ttu-id="d0da3-126">Contém definições das propriedades listadas como nomes alternativos.</span><span class="sxs-lookup"><span data-stu-id="d0da3-126">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="d0da3-127">Confira também</span><span class="sxs-lookup"><span data-stu-id="d0da3-127">See also</span></span>



[<span data-ttu-id="d0da3-128">Propriedades MAPI</span><span class="sxs-lookup"><span data-stu-id="d0da3-128">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="d0da3-129">Propriedades MAPI canônicas</span><span class="sxs-lookup"><span data-stu-id="d0da3-129">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="d0da3-130">Mapear nomes de propriedades canônicas para nomes MAPI</span><span class="sxs-lookup"><span data-stu-id="d0da3-130">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="d0da3-131">Mapear nomes MAPI para nomes de propriedades canônicas</span><span class="sxs-lookup"><span data-stu-id="d0da3-131">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

