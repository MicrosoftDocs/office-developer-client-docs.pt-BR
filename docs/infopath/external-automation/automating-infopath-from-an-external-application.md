---
title: Automatizando o InfoPath de um aplicativo externo
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
ms.assetid: 4d2248d9-ab20-bcaa-d75b-62876c5e95eb
description: Microsoft InfoPath fornece automação de aplicativo do código escrito usando o script e COM usando os métodos do objeto Application e a coleção XDocuments.
ms.openlocfilehash: 0e3fcc50ec11f5fc8791d37144767bf0398ccda7
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19765495"
---
# <a name="automating-infopath-from-an-external-application"></a><span data-ttu-id="1313e-103">Automatizando o InfoPath de um aplicativo externo</span><span class="sxs-lookup"><span data-stu-id="1313e-103">Automating InfoPath from an external application</span></span>

<span data-ttu-id="1313e-104">Microsoft InfoPath fornece automação de aplicativo do código escrito usando o script e COM usando os métodos do objeto **Application** e a coleção **XDocuments** .</span><span class="sxs-lookup"><span data-stu-id="1313e-104">Microsoft InfoPath provides application automation from code written using COM and script by using methods of the **Application** object and the **XDocuments** collection.</span></span> 
  
## <a name="overview-of-the-application-and-xdocument-objects"></a><span data-ttu-id="1313e-105">Visão geral do aplicativo e objetos XDocument</span><span class="sxs-lookup"><span data-stu-id="1313e-105">Overview of the Application and XDocument Objects</span></span>

<span data-ttu-id="1313e-106">O objeto **Application** contém os seguintes métodos usados para automação:</span><span class="sxs-lookup"><span data-stu-id="1313e-106">The **Application** object contains the following methods used for automation:</span></span> 
  
|<span data-ttu-id="1313e-107">**Method**</span><span class="sxs-lookup"><span data-stu-id="1313e-107">**Method**</span></span>|<span data-ttu-id="1313e-108">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="1313e-108">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="1313e-109">**CacheSolution**</span><span class="sxs-lookup"><span data-stu-id="1313e-109">**CacheSolution**</span></span> <br/> |<span data-ttu-id="1313e-110">Examina no cache e, se necessário, atualiza a partir do local publicado do modelo de formulário.</span><span class="sxs-lookup"><span data-stu-id="1313e-110">Examines the in the cache and, if necessary, updates it from the published location of the form template.</span></span>  <br/> |
|<span data-ttu-id="1313e-111">**Quit**</span><span class="sxs-lookup"><span data-stu-id="1313e-111">**Quit**</span></span> <br/> |<span data-ttu-id="1313e-112">Encerra o aplicativo do Microsoft Office InfoPath.</span><span class="sxs-lookup"><span data-stu-id="1313e-112">Quits the Microsoft Office InfoPath application.</span></span>  <br/> |
|<span data-ttu-id="1313e-113">**RegisterSolution**</span><span class="sxs-lookup"><span data-stu-id="1313e-113">**RegisterSolution**</span></span> <br/> |<span data-ttu-id="1313e-114">Instala o modelo de formulário especificado do Microsoft Office InfoPath.</span><span class="sxs-lookup"><span data-stu-id="1313e-114">Installs the specified Microsoft Office InfoPath form template.</span></span>  <br/> |
|<span data-ttu-id="1313e-115">**UnregisterSolution**</span><span class="sxs-lookup"><span data-stu-id="1313e-115">**UnregisterSolution**</span></span> <br/> |<span data-ttu-id="1313e-116">Desinstala o modelo de formulário especificado do Microsoft Office InfoPath.</span><span class="sxs-lookup"><span data-stu-id="1313e-116">Uninstalls the specified Microsoft Office InfoPath form template.</span></span>  <br/> |
   
<span data-ttu-id="1313e-117">A coleção **XDocuments** contém os seguintes métodos que podem ser usados para automação externa:</span><span class="sxs-lookup"><span data-stu-id="1313e-117">The **XDocuments** collection contains the following methods that can be used for external automation:</span></span> 
  
|<span data-ttu-id="1313e-118">**Method**</span><span class="sxs-lookup"><span data-stu-id="1313e-118">**Method**</span></span>|<span data-ttu-id="1313e-119">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="1313e-119">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="1313e-120">Método **Close**</span><span class="sxs-lookup"><span data-stu-id="1313e-120">**Close** method</span></span>  <br/> |<span data-ttu-id="1313e-121">Fecha o formulário especificado do Microsoft Office InfoPath.</span><span class="sxs-lookup"><span data-stu-id="1313e-121">Closes the specified Microsoft Office InfoPath form.</span></span>  <br/> |
|<span data-ttu-id="1313e-122">Método **New**</span><span class="sxs-lookup"><span data-stu-id="1313e-122">**New** method</span></span>  <br/> |<span data-ttu-id="1313e-123">Cria um novo formulário do Microsoft Office InfoPath.</span><span class="sxs-lookup"><span data-stu-id="1313e-123">Creates a new Microsoft Office InfoPath form.</span></span>  <br/> |
|<span data-ttu-id="1313e-124">Método **NewFromSolution**</span><span class="sxs-lookup"><span data-stu-id="1313e-124">**NewFromSolution** method</span></span>  <br/> |<span data-ttu-id="1313e-125">Cria um novo formulário do Microsoft Office InfoPath com base no modelo de formulário especificado.</span><span class="sxs-lookup"><span data-stu-id="1313e-125">Creates a new Microsoft Office InfoPath form based on the specified form template.</span></span>  <br/> |
|<span data-ttu-id="1313e-126">Método **NewFromSolutionWithData**</span><span class="sxs-lookup"><span data-stu-id="1313e-126">**NewFromSolutionWithData** method</span></span>  <br/> |<span data-ttu-id="1313e-127">Cria um novo formulário do Microsoft Office InfoPath usando o modelo de formulário e de dados XML especificado.</span><span class="sxs-lookup"><span data-stu-id="1313e-127">Creates a new Microsoft Office InfoPath form using the specified XML data and form template.</span></span>  <br/> |
|<span data-ttu-id="1313e-128">Método **Open**</span><span class="sxs-lookup"><span data-stu-id="1313e-128">**Open** method</span></span>  <br/> |<span data-ttu-id="1313e-129">Abre o formulário especificado do Microsoft Office InfoPath.</span><span class="sxs-lookup"><span data-stu-id="1313e-129">Opens the specified Microsoft Office InfoPath form.</span></span>  <br/> |
   
<span data-ttu-id="1313e-130">Para usar o objeto **Application** de um aplicativo externo, use a função **CreateObject** com o ProgID do aplicativo InfoPath ("InfoPath.Application") para criar uma variável de objeto que representa o aplicativo do InfoPath.</span><span class="sxs-lookup"><span data-stu-id="1313e-130">To use the **Application** object from an external application, you use the **CreateObject** function with the ProgID of the InfoPath application ("InfoPath.Application") to create an object variable that represents the InfoPath application.</span></span> <span data-ttu-id="1313e-131">Em seguida, você pode usar a propriedade **XDocuments** para acessar a coleção **XDocuments** e usar seus métodos para abrir ou criar um formulário do InfoPath.</span><span class="sxs-lookup"><span data-stu-id="1313e-131">You can then use the **XDocuments** property to access the **XDocuments** collection and use its methods to open or create an InfoPath form.</span></span> <span data-ttu-id="1313e-132">O exemplo a seguir demonstra a criação de uma referência ao objeto de **aplicativo** usando o Microsoft Visual Basic 6.0 ou o Visual Basic for Applications (VBA) linguagem de programação:</span><span class="sxs-lookup"><span data-stu-id="1313e-132">The following example demonstrates the creation of a reference to the **Application** object using the Microsoft Visual Basic 6.0 or Visual Basic for Applications (VBA) programming language:</span></span> 
  
```vb
Dim objIP As Object 
 
Set objIP = CreateObject("InfoPath.Application") 
 
' Open an existing form 
objIP.XDocuments.Open ("C:\MyFolder\MyForm.xml") 
 
' Create a new form based on a form template 
objIP.XDocuments.NewFromSolution ("C:\MyFolder\MyForm.xsn") 

```

> [!NOTE]
> <span data-ttu-id="1313e-133">Como a função **CreateObject** cria uma variável de objeto usando a associação tardia, conclusão da instrução automática não estará disponível no Editor do Visual Basic.</span><span class="sxs-lookup"><span data-stu-id="1313e-133">Because the **CreateObject** function creates an object variable using late binding, automatic statement completion will not be available in the Visual Basic Editor.</span></span> <span data-ttu-id="1313e-134">Consulte os links nas tabelas anteriores para obter informações sobre a sintaxe correta de chamada.</span><span class="sxs-lookup"><span data-stu-id="1313e-134">Refer to the links in the preceding tables for information about the correct calling syntax.</span></span> 
  

