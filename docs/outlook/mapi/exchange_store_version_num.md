---
title: EXCHANGE_STORE_VERSION_NUM
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 88950eda-85ae-ad7a-46c6-0e1933d35e04
description: 'Última modificação: 23 de julho de 2011'
ms.openlocfilehash: bf60b12a6e4575d3504a112aa2b54fb8c4ae23c7
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33433721"
---
# <a name="exchange_store_version_num"></a><span data-ttu-id="4264a-103">EXCHANGE_STORE_VERSION_NUM</span><span class="sxs-lookup"><span data-stu-id="4264a-103">EXCHANGE_STORE_VERSION_NUM</span></span>

  
  
<span data-ttu-id="4264a-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="4264a-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="4264a-105">Armazena informações de versão para o Microsoft Exchange Server que contas em um perfil do Microsoft Office Outlook estão conectadas.</span><span class="sxs-lookup"><span data-stu-id="4264a-105">Stores version information for the Microsoft Exchange Server that accounts in a Microsoft Office Outlook profile are connected to.</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="4264a-106">Informações rápidas</span><span class="sxs-lookup"><span data-stu-id="4264a-106">Quick info</span></span>

```cpp
typedef struct { 
    WORD wMajorVersion; 
    WORD wMinorVersion; 
    WORD wBuild; 
    WORD wMinorBuild; 
} EXCHANGE_STORE_VERSION_NUM; 

```

## <a name="members"></a><span data-ttu-id="4264a-107">Membros</span><span class="sxs-lookup"><span data-stu-id="4264a-107">Members</span></span>

 <span data-ttu-id="4264a-108">_wMajorVersion_</span><span class="sxs-lookup"><span data-stu-id="4264a-108">_wMajorVersion_</span></span>
  
- <span data-ttu-id="4264a-109">Número da versão principal que geralmente é incrementado quando uma versão contém novos recursos significativos e alterações na funcionalidade.</span><span class="sxs-lookup"><span data-stu-id="4264a-109">Major version number that is generally incremented when a release contains significant new features and changes in functionality.</span></span>
    
 <span data-ttu-id="4264a-110">_wMinorVersion_</span><span class="sxs-lookup"><span data-stu-id="4264a-110">_wMinorVersion_</span></span>
  
- <span data-ttu-id="4264a-111">Número de versão secundária que corresponde a um número de versão principal específico e que geralmente é incrementado quando uma versão contém pequenos recursos novos ou correções significativas.</span><span class="sxs-lookup"><span data-stu-id="4264a-111">Minor version number that corresponds to a specific major version number and that is generally incremented when a release contains minor new features or significant fixes.</span></span>
    
 <span data-ttu-id="4264a-112">_wBuild_</span><span class="sxs-lookup"><span data-stu-id="4264a-112">_wBuild_</span></span>
  
- <span data-ttu-id="4264a-113">Número de com build principal que corresponde a números de versão principais e secundárias específicos e que geralmente é incrementado em uma versão interna que contém novos recursos ou correções.</span><span class="sxs-lookup"><span data-stu-id="4264a-113">Major build number that corresponds to specific major and minor version numbers and that is generally incremented in an internal release that contains new features or fixes.</span></span> <span data-ttu-id="4264a-114">Esse valor também é incrementado quando a versão é uma ramificação de código interna importante ou um marco, como um candidato de versão.</span><span class="sxs-lookup"><span data-stu-id="4264a-114">This value is also incremented when the release is a major internal code branch or milestone, such as a release candidate.</span></span>
    
 <span data-ttu-id="4264a-115">_wMinorBuild_</span><span class="sxs-lookup"><span data-stu-id="4264a-115">_wMinorBuild_</span></span>
  
- <span data-ttu-id="4264a-116">Número de com build secundário que geralmente é incrementado em uma versão interna que contém novos recursos ou correções correspondentes a uma com build principal específica que denota uma ramificação ou etapa de código principal.</span><span class="sxs-lookup"><span data-stu-id="4264a-116">Minor build number that is generally incremented in an internal release that contains new features or fixes corresponding to a specific major build that denotes a major code branch or milestone.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="4264a-117">Confira também</span><span class="sxs-lookup"><span data-stu-id="4264a-117">See also</span></span>



[<span data-ttu-id="4264a-118">Sobre as adições de MAPI</span><span class="sxs-lookup"><span data-stu-id="4264a-118">About MAPI Additions</span></span>](about-mapi-additions.md)
  
[<span data-ttu-id="4264a-119">Propriedade canônica PidTagProfileServerFullVersion</span><span class="sxs-lookup"><span data-stu-id="4264a-119">PidTagProfileServerFullVersion Canonical Property</span></span>](pidtagprofileserverfullversion-canonical-property.md)

