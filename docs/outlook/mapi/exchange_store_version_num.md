---
title: EXCHANGE_STORE_VERSION_NUM
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 88950eda-85ae-ad7a-46c6-0e1933d35e04
description: '�ltima altera��o: s�bado, 23 de julho de 2011'
ms.openlocfilehash: 152afd68bea44f3485b2cc566f3f0d2768590704
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22594471"
---
# <a name="exchangestoreversionnum"></a><span data-ttu-id="3c719-103">EXCHANGE_STORE_VERSION_NUM</span><span class="sxs-lookup"><span data-stu-id="3c719-103">EXCHANGE_STORE_VERSION_NUM</span></span>

  
  
<span data-ttu-id="3c719-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="3c719-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="3c719-105">Armazena informações de versão do Microsoft Exchange Server conectados a contas em um perfil do Microsoft Office Outlook.</span><span class="sxs-lookup"><span data-stu-id="3c719-105">Stores version information for the Microsoft Exchange Server that accounts in a Microsoft Office Outlook profile are connected to.</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="3c719-106">Informações rápidas</span><span class="sxs-lookup"><span data-stu-id="3c719-106">Quick info</span></span>

```cpp
typedef struct { 
    WORD wMajorVersion; 
    WORD wMinorVersion; 
    WORD wBuild; 
    WORD wMinorBuild; 
} EXCHANGE_STORE_VERSION_NUM; 

```

## <a name="members"></a><span data-ttu-id="3c719-107">Members</span><span class="sxs-lookup"><span data-stu-id="3c719-107">Members</span></span>

 <span data-ttu-id="3c719-108">_wMajorVersion_</span><span class="sxs-lookup"><span data-stu-id="3c719-108">_wMajorVersion_</span></span>
  
- <span data-ttu-id="3c719-109">Número da versão principal que geralmente é incrementado quando uma versão contém alterações e novos recursos significativos em termos de funcionalidade.</span><span class="sxs-lookup"><span data-stu-id="3c719-109">Major version number that is generally incremented when a release contains significant new features and changes in functionality.</span></span>
    
 <span data-ttu-id="3c719-110">_wMinorVersion_</span><span class="sxs-lookup"><span data-stu-id="3c719-110">_wMinorVersion_</span></span>
  
- <span data-ttu-id="3c719-111">Número de versão secundária que corresponde a um número específico de versão principal e que geralmente é incrementado quando uma versão contém secundárias novos recursos ou correções significativas.</span><span class="sxs-lookup"><span data-stu-id="3c719-111">Minor version number that corresponds to a specific major version number and that is generally incremented when a release contains minor new features or significant fixes.</span></span>
    
 <span data-ttu-id="3c719-112">_wBuild_</span><span class="sxs-lookup"><span data-stu-id="3c719-112">_wBuild_</span></span>
  
- <span data-ttu-id="3c719-113">Número de compilação principais que corresponde aos números de versão principal e secundária específica e que geralmente é incrementado uma versão interna que contém os novos recursos ou correções.</span><span class="sxs-lookup"><span data-stu-id="3c719-113">Major build number that corresponds to specific major and minor version numbers and that is generally incremented in an internal release that contains new features or fixes.</span></span> <span data-ttu-id="3c719-114">Esse valor também é incrementado quando a versão é uma ramificação principais de código interno ou etapa, como uma versão release candidate.</span><span class="sxs-lookup"><span data-stu-id="3c719-114">This value is also incremented when the release is a major internal code branch or milestone, such as a release candidate.</span></span>
    
 <span data-ttu-id="3c719-115">_wMinorBuild_</span><span class="sxs-lookup"><span data-stu-id="3c719-115">_wMinorBuild_</span></span>
  
- <span data-ttu-id="3c719-116">Número de compilação secundária que geralmente é incrementado uma versão interna que contém novos recursos ou corrige correspondente a uma compilação principal específica que denota uma filial principais de código ou etapa do projeto.</span><span class="sxs-lookup"><span data-stu-id="3c719-116">Minor build number that is generally incremented in an internal release that contains new features or fixes corresponding to a specific major build that denotes a major code branch or milestone.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="3c719-117">Confira também</span><span class="sxs-lookup"><span data-stu-id="3c719-117">See also</span></span>



[<span data-ttu-id="3c719-118">Sobre as adições de MAPI</span><span class="sxs-lookup"><span data-stu-id="3c719-118">About MAPI Additions</span></span>](about-mapi-additions.md)
  
[<span data-ttu-id="3c719-119">Propriedade canônica PidTagProfileServerFullVersion</span><span class="sxs-lookup"><span data-stu-id="3c719-119">PidTagProfileServerFullVersion Canonical Property</span></span>](pidtagprofileserverfullversion-canonical-property.md)

