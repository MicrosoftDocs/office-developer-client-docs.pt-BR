---
title: Referência do desenvolvedor do OneNote
manager: soliver
ms.date: 05/16/2016
ms.audience: Developer
localization_priority: Normal
ms.assetid: 4c4ef9e8-6b30-481b-8023-2e1280bcbcc9
description: Esta referência contém visões gerais conceituais e programáticas referências para guiá-lo no desenvolvimento de soluções para aplicativos de cliente de desktop do OneNote 2013.
ms.openlocfilehash: 6a3dde524dfa5357c4523db3b545ac583eaa3274
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22566576"
---
# <a name="onenote-developer-reference"></a><span data-ttu-id="43fcd-103">Referência do desenvolvedor do OneNote</span><span class="sxs-lookup"><span data-stu-id="43fcd-103">OneNote developer reference</span></span>

<span data-ttu-id="43fcd-104">Esta referência contém visões gerais conceituais e programáticas referências para guiá-lo no desenvolvimento de soluções para aplicativos de cliente de desktop do OneNote 2013.</span><span class="sxs-lookup"><span data-stu-id="43fcd-104">This reference contains conceptual overviews and programmatic references to guide you in developing solutions for OneNote 2013 desktop client applications.</span></span> <span data-ttu-id="43fcd-105">Inclui todas as adições e altera para a interface de programação de aplicativo (API) do OneNote 2013 e fornece exemplos de códigos em c# para mostrar como executar algumas tarefas no OneNote.</span><span class="sxs-lookup"><span data-stu-id="43fcd-105">It includes all the additions and changes to the OneNote 2013 application programming interface (API), and provides code samples in C# to show how to perform some tasks in OneNote.</span></span> <span data-ttu-id="43fcd-106">A API do OneNote 2013 permite aos usuários programaticamente acessar e editar o conteúdo do OneNote.</span><span class="sxs-lookup"><span data-stu-id="43fcd-106">The OneNote 2013 API enables users to programmatically access and edit OneNote content.</span></span> <span data-ttu-id="43fcd-107">Os usuários também podem fazer alterações ao modo de exibição de janelas do OneNote.</span><span class="sxs-lookup"><span data-stu-id="43fcd-107">Users can also make changes to the view of OneNote windows.</span></span>
  
<span data-ttu-id="43fcd-108">Esta documentação contém as seguintes informações:</span><span class="sxs-lookup"><span data-stu-id="43fcd-108">This documentation contains the following information:</span></span>
  
- <span data-ttu-id="43fcd-109">[Interfaces de janela](window-interfaces-onenote.md): descreve as interfaces de **janela** e **janelas** , que permitem aos usuários enumerar toda o conjunto de janelas do OneNote e modificar determinadas propriedades de janela.</span><span class="sxs-lookup"><span data-stu-id="43fcd-109">[Window interfaces](window-interfaces-onenote.md): Describes the **Window** and **Windows** interfaces, which enable users to enumerate through the set of OneNote windows and modify certain window properties.</span></span> 
    
- <span data-ttu-id="43fcd-110">[Interfaces de caixa de diálogo arquivamento rápido](quick-filing-dialog-box-interfaces-onenote.md): descreve as interfaces que você pode usar para personalizar programaticamente a caixa de diálogo **Arquivamento rápido** no OneNote 2013.</span><span class="sxs-lookup"><span data-stu-id="43fcd-110">[Quick Filing dialog box interfaces](quick-filing-dialog-box-interfaces-onenote.md): Describes the interfaces that you can use to programmatically customize the **Quick Filing** dialog box in OneNote 2013.</span></span> 
    
- <span data-ttu-id="43fcd-111">[Interface do aplicativo](application-interface-onenote.md): descreve os métodos, propriedades e eventos que ajudam a recuperar, manipular e atualizar informações do OneNote 2013 e o conteúdo.</span><span class="sxs-lookup"><span data-stu-id="43fcd-111">[Application interface](application-interface-onenote.md): Describes methods, properties, and events that help retrieve, manipulate, and update OneNote 2013 information and content.</span></span>
    
- <span data-ttu-id="43fcd-112">[Enumerações](enumerations-onenote-developer-reference.md): descreve as enumerações no modelo de objeto do OneNote 2013.</span><span class="sxs-lookup"><span data-stu-id="43fcd-112">[Enumerations](enumerations-onenote-developer-reference.md): Describes the enumerations in the OneNote 2013 object model.</span></span>
    
- <span data-ttu-id="43fcd-113">[Códigos de erro](error-codes-onenote.md): lista os códigos de erro no modelo de objeto do OneNote 2013.</span><span class="sxs-lookup"><span data-stu-id="43fcd-113">[Error codes](error-codes-onenote.md): Lists the error codes in the OneNote 2013 object model.</span></span>
    
> [!NOTE]
> <span data-ttu-id="43fcd-114">As APIs descritas nesta documentação destinam-se apenas para soluções de cliente de área de trabalho do OneNote Win32 em cenários não conectados.</span><span class="sxs-lookup"><span data-stu-id="43fcd-114">The APIs described in this documentation are intended only for OneNote Win32 desktop client solutions in unconnected scenarios.</span></span> <span data-ttu-id="43fcd-115">Para cenários conectados, use as APIs de serviço recomendadas do OneNote.</span><span class="sxs-lookup"><span data-stu-id="43fcd-115">For connected scenarios, use the recommended OneNote service APIs.</span></span> <span data-ttu-id="43fcd-116">Para saber mais, visite [dev.onenote.com](http://go.microsoft.com/fwlink/?LinkID=390615).</span><span class="sxs-lookup"><span data-stu-id="43fcd-116">To learn more, visit [dev.onenote.com](http://go.microsoft.com/fwlink/?LinkID=390615).</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="43fcd-117">Confira também</span><span class="sxs-lookup"><span data-stu-id="43fcd-117">See also</span></span>

- [<span data-ttu-id="43fcd-118">OneNote para desenvolvedores</span><span class="sxs-lookup"><span data-stu-id="43fcd-118">OneNote for developers</span></span>](http://go.microsoft.com/fwlink/?LinkID=390615)   
- <span data-ttu-id="43fcd-119">[Exemplos de GitHub](https://github.com/OneNoteDev/) (Serviço APIs do OneNote)</span><span class="sxs-lookup"><span data-stu-id="43fcd-119">[Samples on GitHub](https://github.com/OneNoteDev/) (OneNote service APIs)</span></span>     
- [<span data-ttu-id="43fcd-120">Accessibility in Microsoft Products</span><span class="sxs-lookup"><span data-stu-id="43fcd-120">Accessibility in Microsoft Products</span></span>](http://www.microsoft.com/enable/products/default.aspx)    
- [<span data-ttu-id="43fcd-121">Convenções de Documentos</span><span class="sxs-lookup"><span data-stu-id="43fcd-121">Document Conventions</span></span>](http://msdn.microsoft.com/en-us/office/aa905365.aspx)    
- [<span data-ttu-id="43fcd-122">Informações de direitos autorais de referência do desenvolvedor do OneNote</span><span class="sxs-lookup"><span data-stu-id="43fcd-122">OneNote Developer Reference Copyright Information</span></span>](https://msdn.microsoft.com/en-us/library/office/jj680116.aspx)
    
    

