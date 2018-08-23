---
title: FixMAPI
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 32676003-ba32-886f-1185-4760cb0e30e3
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: 863e401f66a8012b3bd9954ed56c02382f1bd4e2
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22565932"
---
# <a name="fixmapi"></a><span data-ttu-id="3f6b8-103">FixMAPI</span><span class="sxs-lookup"><span data-stu-id="3f6b8-103">FixMAPI</span></span>

  
  
<span data-ttu-id="3f6b8-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="3f6b8-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="3f6b8-105">Faz uma cópia de backup da cópia atual do MAPI32 no cliente, computador e restaura Mapi32 com a biblioteca stub MAPI, Mapistub.</span><span class="sxs-lookup"><span data-stu-id="3f6b8-105">Makes a backup copy of the current copy of mapi32.dll on the client computer, and restores mapi32.dll with the MAPI stub library, mapistub.dll.</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="3f6b8-106">Informações rápidas</span><span class="sxs-lookup"><span data-stu-id="3f6b8-106">Quick info</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="3f6b8-107">Exportá-los por:</span><span class="sxs-lookup"><span data-stu-id="3f6b8-107">Exported by:</span></span>  <br/> |<span data-ttu-id="3f6b8-108">Mapistub</span><span class="sxs-lookup"><span data-stu-id="3f6b8-108">mapistub.dll</span></span>  <br/> |
|<span data-ttu-id="3f6b8-109">Chamado pelo:</span><span class="sxs-lookup"><span data-stu-id="3f6b8-109">Called by:</span></span>  <br/> |<span data-ttu-id="3f6b8-110">Cliente</span><span class="sxs-lookup"><span data-stu-id="3f6b8-110">Client</span></span>  <br/> |
|<span data-ttu-id="3f6b8-111">Implementada por:</span><span class="sxs-lookup"><span data-stu-id="3f6b8-111">Implemented by:</span></span>  <br/> |<span data-ttu-id="3f6b8-112">Windows</span><span class="sxs-lookup"><span data-stu-id="3f6b8-112">Windows</span></span>  <br/> |
   
```cpp
DWORD STDAPICALLTYPE FixMAPI(void); 
```

## <a name="return-values"></a><span data-ttu-id="3f6b8-113">Valores de retorno</span><span class="sxs-lookup"><span data-stu-id="3f6b8-113">Return values</span></span>

<span data-ttu-id="3f6b8-114">Se a função tiver êxito, o valor de retorno é um valor diferente de zero.</span><span class="sxs-lookup"><span data-stu-id="3f6b8-114">If the function succeeds, the return value is a non-zero value.</span></span>
  
<span data-ttu-id="3f6b8-115">Se a função falhar, o valor de retorno é zero.</span><span class="sxs-lookup"><span data-stu-id="3f6b8-115">If the function fails, the return value is zero.</span></span> <span data-ttu-id="3f6b8-116">Para obter informações de erro estendidas, chame a função de Software Development Kit (SDK) do Microsoft Windows, **[GetLastError](http://msdn.microsoft.com/en-us/library/ms679360.aspx)**.</span><span class="sxs-lookup"><span data-stu-id="3f6b8-116">To get extended error information, call the Microsoft Windows Software Development Kit (SDK) function, **[GetLastError](http://msdn.microsoft.com/en-us/library/ms679360.aspx)**.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="3f6b8-117">Comentários</span><span class="sxs-lookup"><span data-stu-id="3f6b8-117">Remarks</span></span>

 <span data-ttu-id="3f6b8-118">**FixMAPI** não substitui o arquivo Mapi32 atual se o arquivo está marcado como somente leitura.</span><span class="sxs-lookup"><span data-stu-id="3f6b8-118">**FixMAPI** does not replace the current mapi32.dll file if the file is marked as read-only.</span></span> 
  
 <span data-ttu-id="3f6b8-119">**FixMAPI** não substitui o Mapi32 atual se o Microsoft Exchange Server estiver instalado no computador.</span><span class="sxs-lookup"><span data-stu-id="3f6b8-119">**FixMAPI** does not replace the current mapi32.dll if Microsoft Exchange Server is installed on the computer.</span></span> 
  
<span data-ttu-id="3f6b8-120">Quando **FixMAPI** faz uma cópia de backup da cópia atual do MAPI32 no computador, ele atribui a cópia de backup um nome diferente do "Mapi32".</span><span class="sxs-lookup"><span data-stu-id="3f6b8-120">When **FixMAPI** makes a backup copy of the current copy of mapi32.dll on the computer, it assigns the backup copy a name different from "mapi32.dll".</span></span> <span data-ttu-id="3f6b8-121">Ele, em seguida, direciona as chamadas subsequentes destinadas a nesse assembly para a cópia de backup.</span><span class="sxs-lookup"><span data-stu-id="3f6b8-121">It then directs subsequent calls intended for that assembly to the backup copy.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="3f6b8-122">Confira também</span><span class="sxs-lookup"><span data-stu-id="3f6b8-122">See also</span></span>



[<span data-ttu-id="3f6b8-123">KB 256946: Você recebe uma mensagem de erro de conflito do programa quando você inicia o Outlook 2000</span><span class="sxs-lookup"><span data-stu-id="3f6b8-123">KB 256946: You receive a program conflict error message when you start Outlook 2000</span></span>](http://support.microsoft.com/kb/256946)
  
[<span data-ttu-id="3f6b8-124">KB 228457: Descrição da ferramenta Fixmapi.exe incluída com o Internet Explorer 5</span><span class="sxs-lookup"><span data-stu-id="3f6b8-124">KB 228457: Description of the Fixmapi.exe Tool Included with Internet Explorer 5</span></span>](http://support.microsoft.com/kb/228457)

