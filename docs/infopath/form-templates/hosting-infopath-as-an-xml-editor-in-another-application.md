---
title: Hospedando InfoPath como um Editor de XML em outro aplicativo
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
ms.assetid: ae24b317-f486-763a-7009-e32c5cb85b59
description: O ambiente de edição de formulários do Microsoft InfoPath podem ser hospedado em um aplicativo personalizado do Windows, que permite aos desenvolvedores integrar o ambiente em aplicativos de linha de negócios de edição de formulários do InfoPath.
ms.openlocfilehash: dd87cba7219b5647bd2b20dd67c6eb0f1811cc59
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19765595"
---
# <a name="hosting-infopath-as-an-xml-editor-in-another-application"></a><span data-ttu-id="67c4f-103">Hospedando InfoPath como um Editor de XML em outro aplicativo</span><span class="sxs-lookup"><span data-stu-id="67c4f-103">Hosting InfoPath as an XML Editor in Another Application</span></span>

<span data-ttu-id="67c4f-104">O ambiente de edição de formulários do Microsoft InfoPath podem ser hospedado em um aplicativo personalizado do Windows.</span><span class="sxs-lookup"><span data-stu-id="67c4f-104">The Microsoft InfoPath form editing environment can be hosted in a custom Windows application.</span></span> <span data-ttu-id="67c4f-105">Esse recurso permite aos desenvolvedores integrar o ambiente em aplicativos de linha de negócios de edição de formulários do InfoPath.</span><span class="sxs-lookup"><span data-stu-id="67c4f-105">This feature enables developers to integrate the InfoPath form editing environment into line-of-business applications.</span></span> <span data-ttu-id="67c4f-106">Os desenvolvedores que criam aplicativos baseados em COM tradicionais podem usar o objeto de **InfoPathEditorObject** que está disponível pela referência a IPEDITOR. DLL e os desenvolvedores que criam a Microsoft. Aplicativos baseados em NET podem usar o assembly **Microsoft.Office.InfoPath.FormControl** , que fornece tipos gerenciados com base na interface COM.</span><span class="sxs-lookup"><span data-stu-id="67c4f-106">Developers writing traditional COM-based applications can use the **InfoPathEditorObject** object that is available by referencing the IPEDITOR.DLL, and developers writing Microsoft .NET-based applications can use the **Microsoft.Office.InfoPath.FormControl** assembly, which provides managed types based on the COM interface.</span></span> <span data-ttu-id="67c4f-107">O IPEDITOR. DLL e assembly **Microsoft.Office.InfoPath.FormControl** são instalados, juntamente com o InfoPath no C:\Program Files\Microsoft Office\Office15 ou arquivos C:\Program (x86) \Microsoft Office\Office15 pasta.</span><span class="sxs-lookup"><span data-stu-id="67c4f-107">The IPEDITOR.DLL and **Microsoft.Office.InfoPath.FormControl** assembly are both installed along with InfoPath in the C:\Program Files\Microsoft Office\Office15 or C:\Program Files (x86)\Microsoft Office\Office15 folder.</span></span> 
  
<span data-ttu-id="67c4f-108">O artigo MSDN, hospedando o ambiente de edição de formulário do InfoPath 2007 em um aplicativo de formulário personalizado do Windows, enfoca o objeto **FormControl** e como incorporá-la em seu personalizado. Aplicativos baseados em NET.</span><span class="sxs-lookup"><span data-stu-id="67c4f-108">The MSDN article, Hosting the InfoPath 2007 Form Editing Environment in a Custom Windows Form Application, focuses on the **FormControl** object and how to incorporate it into your custom .NET-based applications.</span></span> <span data-ttu-id="67c4f-109">O download associado ao artigo contém um aplicativo personalizado que fornece funções de .NET para replicar o ambiente devido ao uso COM **IOleCommandTargets**de edição de formulários do InfoPath.</span><span class="sxs-lookup"><span data-stu-id="67c4f-109">The download associated with the article contains a custom application that provides .NET functions for replicating the InfoPath form editing environment through the use of COM **IOleCommandTargets**.</span></span>
  

