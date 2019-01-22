---
title: Referência do Desenvolvedor do OneNote
manager: soliver
ms.date: 05/16/2016
ms.audience: Developer
ms.assetid: 4c4ef9e8-6b30-481b-8023-2e1280bcbcc9
description: Esta referência contém uma visão geral conceitual e referências programáticas para orientá-lo no desenvolvimento de soluções para aplicativos cliente para área de trabalho do OneNote 2013.
localization_priority: Priority
ms.openlocfilehash: d2b401a768e62c4b9712b1590bfaf499c2b022ab
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/18/2019
ms.locfileid: "28725921"
---
# <a name="onenote-developer-reference"></a><span data-ttu-id="b3a7e-103">Referência do Desenvolvedor do OneNote</span><span class="sxs-lookup"><span data-stu-id="b3a7e-103">OneNote developer reference</span></span>

<span data-ttu-id="b3a7e-104">Esta referência contém uma visão geral conceitual e referências programáticas para orientá-lo no desenvolvimento de soluções para aplicativos cliente para área de trabalho do OneNote 2013.</span><span class="sxs-lookup"><span data-stu-id="b3a7e-104">This reference contains conceptual overviews and programmatic references to guide you in developing solutions for OneNote 2013 desktop client applications.</span></span> <span data-ttu-id="b3a7e-105">Ela apresenta todas as adições e alterações feitas à API (interface de programação de aplicativo) do OneNote 2013 e fornece exemplos de código em C# para mostrar como realizar algumas tarefas no OneNote.</span><span class="sxs-lookup"><span data-stu-id="b3a7e-105">It includes all the additions and changes to the OneNote 2013 application programming interface (API), and provides code samples in C# to show how to perform some tasks in OneNote.</span></span> <span data-ttu-id="b3a7e-106">A API do OneNote 2013 permite aos usuários acessar e editar de forma programática o conteúdo do OneNote.</span><span class="sxs-lookup"><span data-stu-id="b3a7e-106">The OneNote 2013 API enables users to programmatically access and edit OneNote content.</span></span> <span data-ttu-id="b3a7e-107">Os usuários também podem fazer alterações no modo de exibição de janelas do OneNote.</span><span class="sxs-lookup"><span data-stu-id="b3a7e-107">Users can also make changes to the view of OneNote windows.</span></span>
  
<span data-ttu-id="b3a7e-108">Esta documentação contém as seguintes informações:</span><span class="sxs-lookup"><span data-stu-id="b3a7e-108">This documentation contains the following information:</span></span>
  
- <span data-ttu-id="b3a7e-109">[Interfaces de janela](window-interfaces-onenote.md): descreve as interfaces de**janela** e **janelas** que permitem aos usuários fazer a enumeração por meio do conjunto de janelas do OneNote e a modificação de determinadas propriedades da janela.</span><span class="sxs-lookup"><span data-stu-id="b3a7e-109">[Window interfaces](window-interfaces-onenote.md): Describes the **Window** and **Windows** interfaces, which enable users to enumerate through the set of OneNote windows and modify certain window properties.</span></span> 
    
- <span data-ttu-id="b3a7e-110">[Interfaces de caixa de diálogo do Arquivamento rápido](quick-filing-dialog-box-interfaces-onenote.md): descreve as interfaces disponíveis para personalizar de forma programática a caixa de diálogo **Arquivamento rápido** no OneNote 2013.</span><span class="sxs-lookup"><span data-stu-id="b3a7e-110">[Quick Filing dialog box interfaces](quick-filing-dialog-box-interfaces-onenote.md): Describes the interfaces that you can use to programmatically customize the **Quick Filing** dialog box in OneNote 2013.</span></span> 
    
- <span data-ttu-id="b3a7e-111">[Interface do aplicativo](application-interface-onenote.md): descreve os métodos, as propriedades e os eventos que ajudam a recuperar, manipular e atualizar as informações e o conteúdo do OneNote 2013.</span><span class="sxs-lookup"><span data-stu-id="b3a7e-111">[Application interface](application-interface-onenote.md): Describes methods, properties, and events that help retrieve, manipulate, and update OneNote 2013 information and content.</span></span>
    
- <span data-ttu-id="b3a7e-112">[Enumerações](enumerations-onenote-developer-reference.md): descreve as enumerações no modelo de objeto do OneNote 2013.</span><span class="sxs-lookup"><span data-stu-id="b3a7e-112">[Enumerations](enumerations-onenote-developer-reference.md): Describes the enumerations in the OneNote 2013 object model.</span></span>
    
- <span data-ttu-id="b3a7e-113">[Códigos de erro](error-codes-onenote.md): lista os códigos de erro no modelo de objeto do OneNote 2013.</span><span class="sxs-lookup"><span data-stu-id="b3a7e-113">[Error codes](error-codes-onenote.md): Lists the error codes in the OneNote 2013 object model.</span></span>
    
> [!NOTE]
> <span data-ttu-id="b3a7e-114">As APIs descritas nesta documentação destinam-se apenas a soluções de cliente de área de trabalho do OneNote Win32 em cenários não conectados.</span><span class="sxs-lookup"><span data-stu-id="b3a7e-114">The APIs described in this documentation are intended only for OneNote Win32 desktop client solutions in unconnected scenarios.</span></span> <span data-ttu-id="b3a7e-115">Para cenários conectados, use as APIs de serviço recomendadas do OneNote.</span><span class="sxs-lookup"><span data-stu-id="b3a7e-115">For connected scenarios, use the recommended OneNote service APIs.</span></span> <span data-ttu-id="b3a7e-116">Saiba mais em [dev.onenote.com](https://go.microsoft.com/fwlink/?LinkID=390615).</span><span class="sxs-lookup"><span data-stu-id="b3a7e-116">To learn more, visit [dev.onenote.com](https://go.microsoft.com/fwlink/?LinkID=390615).</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="b3a7e-117">Confira também</span><span class="sxs-lookup"><span data-stu-id="b3a7e-117">See also</span></span>

- [<span data-ttu-id="b3a7e-118">OneNote para desenvolvedores</span><span class="sxs-lookup"><span data-stu-id="b3a7e-118">OneNote for developers</span></span>](https://go.microsoft.com/fwlink/?LinkID=390615)   
- <span data-ttu-id="b3a7e-119">[Exemplos no GitHub](https://github.com/OneNoteDev/) (APIs de serviço do OneNote)</span><span class="sxs-lookup"><span data-stu-id="b3a7e-119">[Samples on GitHub](https://github.com/OneNoteDev/) (OneNote service APIs)</span></span>     
- [<span data-ttu-id="b3a7e-120">Acessibilidade em produtos Microsoft</span><span class="sxs-lookup"><span data-stu-id="b3a7e-120">Accessibility in Microsoft Products</span></span>](https://www.microsoft.com/enable/products/default.aspx)    
- [<span data-ttu-id="b3a7e-121">Convenções de Documentos</span><span class="sxs-lookup"><span data-stu-id="b3a7e-121">Document Conventions</span></span>](https://msdn.microsoft.com/office/aa905365.aspx)    
- [<span data-ttu-id="b3a7e-122">Informações sobre direitos autorais de referência para o desenvolvedor do OneNote</span><span class="sxs-lookup"><span data-stu-id="b3a7e-122">OneNote Developer Reference Copyright Information</span></span>](https://msdn.microsoft.com/library/office/jj680116.aspx)
    
    

