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
ms.openlocfilehash: 2aeca1a65a859ac9502995a463bc4869609bcd15
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32334958"
---
# <a name="fixmapi"></a><span data-ttu-id="a6087-103">FixMAPI</span><span class="sxs-lookup"><span data-stu-id="a6087-103">FixMAPI</span></span>

  
  
<span data-ttu-id="a6087-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="a6087-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="a6087-105">Faz uma cópia de backup da cópia atual mapi32.dll no computador cliente e restaura mapi32.dll com a biblioteca stub MAPI, mapistub.dll.</span><span class="sxs-lookup"><span data-stu-id="a6087-105">Makes a backup copy of the current copy of mapi32.dll on the client computer, and restores mapi32.dll with the MAPI stub library, mapistub.dll.</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="a6087-106">Informações rápidas</span><span class="sxs-lookup"><span data-stu-id="a6087-106">Quick info</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="a6087-107">Exportado por:</span><span class="sxs-lookup"><span data-stu-id="a6087-107">Exported by:</span></span>  <br/> |<span data-ttu-id="a6087-108">mapistub.dll</span><span class="sxs-lookup"><span data-stu-id="a6087-108">mapistub.dll</span></span>  <br/> |
|<span data-ttu-id="a6087-109">Chamado por:</span><span class="sxs-lookup"><span data-stu-id="a6087-109">Called by:</span></span>  <br/> |<span data-ttu-id="a6087-110">Cliente</span><span class="sxs-lookup"><span data-stu-id="a6087-110">Client</span></span>  <br/> |
|<span data-ttu-id="a6087-111">Implementado por:</span><span class="sxs-lookup"><span data-stu-id="a6087-111">Implemented by:</span></span>  <br/> |<span data-ttu-id="a6087-112">Windows</span><span class="sxs-lookup"><span data-stu-id="a6087-112">Windows</span></span>  <br/> |
   
```cpp
DWORD STDAPICALLTYPE FixMAPI(void); 
```

## <a name="return-values"></a><span data-ttu-id="a6087-113">Valor de retorno</span><span class="sxs-lookup"><span data-stu-id="a6087-113">Return values</span></span>

<span data-ttu-id="a6087-114">Se a função for bem-sucedida, o valor de retorno será um valor não zero.</span><span class="sxs-lookup"><span data-stu-id="a6087-114">If the function succeeds, the return value is a non-zero value.</span></span>
  
<span data-ttu-id="a6087-115">Se a função falhar, o valor de retorno será zero.</span><span class="sxs-lookup"><span data-stu-id="a6087-115">If the function fails, the return value is zero.</span></span> <span data-ttu-id="a6087-116">Para obter informações de erro estendidas, chame a função Microsoft Windows Software Development Kit (SDK), **[GetLastError](https://msdn.microsoft.com/library/ms679360.aspx)**.</span><span class="sxs-lookup"><span data-stu-id="a6087-116">To get extended error information, call the Microsoft Windows Software Development Kit (SDK) function, **[GetLastError](https://msdn.microsoft.com/library/ms679360.aspx)**.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="a6087-117">Comentários</span><span class="sxs-lookup"><span data-stu-id="a6087-117">Remarks</span></span>

 <span data-ttu-id="a6087-118">**FixMAPI** não substituirá o arquivo mapi32.dll atual se o arquivo estiver marcado como somente leitura.</span><span class="sxs-lookup"><span data-stu-id="a6087-118">**FixMAPI** does not replace the current mapi32.dll file if the file is marked as read-only.</span></span> 
  
 <span data-ttu-id="a6087-119">**FixMAPI** não substitui o mapi32.dll atual se o Microsoft Exchange Server estiver instalado no computador.</span><span class="sxs-lookup"><span data-stu-id="a6087-119">**FixMAPI** does not replace the current mapi32.dll if Microsoft Exchange Server is installed on the computer.</span></span> 
  
<span data-ttu-id="a6087-120">Quando **FixMAPI** faz uma cópia de backup da cópia atual mapi32.dll no computador, ele atribui à cópia de backup um nome diferente de "mapi32.dll".</span><span class="sxs-lookup"><span data-stu-id="a6087-120">When **FixMAPI** makes a backup copy of the current copy of mapi32.dll on the computer, it assigns the backup copy a name different from "mapi32.dll".</span></span> <span data-ttu-id="a6087-121">Em seguida, ele direciona chamadas subsequentes destinadas a esse assembly para a cópia de backup.</span><span class="sxs-lookup"><span data-stu-id="a6087-121">It then directs subsequent calls intended for that assembly to the backup copy.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="a6087-122">Confira também</span><span class="sxs-lookup"><span data-stu-id="a6087-122">See also</span></span>



[<span data-ttu-id="a6087-123">KB 256946: Você recebe uma mensagem de erro de conflito de programa ao iniciar o Outlook 2000</span><span class="sxs-lookup"><span data-stu-id="a6087-123">KB 256946: You receive a program conflict error message when you start Outlook 2000</span></span>](https://support.microsoft.com/kb/256946)
  
[<span data-ttu-id="a6087-124">KB 228457: Descrição da ferramenta Fixmapi.exe incluída com o Internet Explorer 5</span><span class="sxs-lookup"><span data-stu-id="a6087-124">KB 228457: Description of the Fixmapi.exe Tool Included with Internet Explorer 5</span></span>](https://support.microsoft.com/kb/228457)

