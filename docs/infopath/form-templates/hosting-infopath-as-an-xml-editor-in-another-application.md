---
title: Hospedando o InfoPath como um Editor de XML em outro aplicativo
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
ms.assetid: ae24b317-f486-763a-7009-e32c5cb85b59
description: O ambiente de edição de formulário do Microsoft InfoPath pode ser hospedado em um aplicativo personalizado do Windows, que permite aos desenvolvedores integrar o ambiente de edição de formulário do InfoPath a aplicativos de linha de negócios.
ms.openlocfilehash: b85e47d506b17982bb883c9d56ea13131807d1cf
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33422576"
---
# <a name="hosting-infopath-as-an-xml-editor-in-another-application"></a><span data-ttu-id="e64f6-103">Hospedando o InfoPath como um Editor de XML em outro aplicativo</span><span class="sxs-lookup"><span data-stu-id="e64f6-103">Hosting InfoPath as an XML Editor in Another Application</span></span>

<span data-ttu-id="e64f6-104">O ambiente de edição de formulário do Microsoft InfoPath pode ser hospedado em um aplicativo personalizado do Windows.</span><span class="sxs-lookup"><span data-stu-id="e64f6-104">The Microsoft InfoPath form editing environment can be hosted in a custom Windows application.</span></span> <span data-ttu-id="e64f6-105">Esse recurso permite que os desenvolvedores integrem o ambiente de edição de formulário do InfoPath em aplicativos de linha de negócios.</span><span class="sxs-lookup"><span data-stu-id="e64f6-105">This feature enables developers to integrate the InfoPath form editing environment into line-of-business applications.</span></span> <span data-ttu-id="e64f6-106">Os desenvolvedores que escrevem aplicativos baseados em COM tradicionais podem usar o objeto **InfoPathEditorObject** que está disponível referenciando o IPEDITOR.DLL e os desenvolvedores escrevendo microsoft . Aplicativos baseados em NET podem usar o assembly **Microsoft.Office.InfoPath.FormControl,** que fornece tipos gerenciados com base na interface COM.</span><span class="sxs-lookup"><span data-stu-id="e64f6-106">Developers writing traditional COM-based applications can use the **InfoPathEditorObject** object that is available by referencing the IPEDITOR.DLL, and developers writing Microsoft .NET-based applications can use the **Microsoft.Office.InfoPath.FormControl** assembly, which provides managed types based on the COM interface.</span></span> <span data-ttu-id="e64f6-107">Os assemblys IPEDITOR.DLL e **Microsoft.Office.InfoPath.FormControl** são instalados junto com o InfoPath na pasta C:\Arquivos de Programas\Microsoft Office\Office15 ou C:\Arquivos de Programas (x86)\Microsoft Office\Office15.</span><span class="sxs-lookup"><span data-stu-id="e64f6-107">The IPEDITOR.DLL and **Microsoft.Office.InfoPath.FormControl** assembly are both installed along with InfoPath in the C:\Program Files\Microsoft Office\Office15 or C:\Program Files (x86)\Microsoft Office\Office15 folder.</span></span> 
  
<span data-ttu-id="e64f6-108">O artigo MSDN, hospedando o InfoPath 2007 Form Editing Environment em um aplicativo de formulário personalizado do Windows, concentra-se no objeto **FormControl** e como incorporá-lo ao seu personalizado . Aplicativos baseados em NET.</span><span class="sxs-lookup"><span data-stu-id="e64f6-108">The MSDN article, Hosting the InfoPath 2007 Form Editing Environment in a Custom Windows Form Application, focuses on the **FormControl** object and how to incorporate it into your custom .NET-based applications.</span></span> <span data-ttu-id="e64f6-109">O download associado ao artigo contém um aplicativo personalizado que fornece funções .NET para replicar o ambiente de edição de formulário do InfoPath por meio do uso de **COM IOleCommandTargets**.</span><span class="sxs-lookup"><span data-stu-id="e64f6-109">The download associated with the article contains a custom application that provides .NET functions for replicating the InfoPath form editing environment through the use of COM **IOleCommandTargets**.</span></span>
  

