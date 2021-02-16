---
title: Automatizar o InfoPath desde aplicativos externos
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
ms.assetid: 4d2248d9-ab20-bcaa-d75b-62876c5e95eb
description: O Microsoft InfoPath fornece automação de aplicativo do código escrito usando COM e script usando métodos do objeto Application e da coleção XDocuments.
ms.openlocfilehash: 7eccbca34b93aff7909de92eebc04d012d4dd97c
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33412664"
---
# <a name="automating-infopath-from-an-external-application"></a><span data-ttu-id="d6630-103">Automatizar o InfoPath desde aplicativos externos</span><span class="sxs-lookup"><span data-stu-id="d6630-103">Automating InfoPath from an external application</span></span>

<span data-ttu-id="d6630-104">O Microsoft InfoPath fornece automação de aplicativo do código escrito usando COM e script usando métodos do objeto **Application** e da **coleção XDocuments.**</span><span class="sxs-lookup"><span data-stu-id="d6630-104">Microsoft InfoPath provides application automation from code written using COM and script by using methods of the **Application** object and the **XDocuments** collection.</span></span> 
  
## <a name="overview-of-the-application-and-xdocument-objects"></a><span data-ttu-id="d6630-105">Visão geral dos objetos Application e XDocument</span><span class="sxs-lookup"><span data-stu-id="d6630-105">Overview of the Application and XDocument Objects</span></span>

<span data-ttu-id="d6630-106">O **objeto Application** contém os seguintes métodos usados para automação:</span><span class="sxs-lookup"><span data-stu-id="d6630-106">The **Application** object contains the following methods used for automation:</span></span> 
  
|<span data-ttu-id="d6630-107">**Method**</span><span class="sxs-lookup"><span data-stu-id="d6630-107">**Method**</span></span>|<span data-ttu-id="d6630-108">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="d6630-108">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="d6630-109">**CacheSolution**</span><span class="sxs-lookup"><span data-stu-id="d6630-109">**CacheSolution**</span></span> <br/> |<span data-ttu-id="d6630-110">Examina o arquivo no cache e, se necessário, atualiza-o do local publicado do modelo de formulário.</span><span class="sxs-lookup"><span data-stu-id="d6630-110">Examines the in the cache and, if necessary, updates it from the published location of the form template.</span></span>  <br/> |
|<span data-ttu-id="d6630-111">**Quit**</span><span class="sxs-lookup"><span data-stu-id="d6630-111">**Quit**</span></span> <br/> |<span data-ttu-id="d6630-112">Sai do aplicativo Microsoft Office InfoPath.</span><span class="sxs-lookup"><span data-stu-id="d6630-112">Quits the Microsoft Office InfoPath application.</span></span>  <br/> |
|<span data-ttu-id="d6630-113">**RegisterSolution**</span><span class="sxs-lookup"><span data-stu-id="d6630-113">**RegisterSolution**</span></span> <br/> |<span data-ttu-id="d6630-114">Instala o modelo de formulário do Microsoft Office InfoPath especificado.</span><span class="sxs-lookup"><span data-stu-id="d6630-114">Installs the specified Microsoft Office InfoPath form template.</span></span>  <br/> |
|<span data-ttu-id="d6630-115">**UnregisterSolution**</span><span class="sxs-lookup"><span data-stu-id="d6630-115">**UnregisterSolution**</span></span> <br/> |<span data-ttu-id="d6630-116">Desinstala o modelo de formulário do Microsoft Office InfoPath especificado.</span><span class="sxs-lookup"><span data-stu-id="d6630-116">Uninstalls the specified Microsoft Office InfoPath form template.</span></span>  <br/> |
   
<span data-ttu-id="d6630-117">A **coleção XDocuments** contém os seguintes métodos que podem ser usados para automação externa:</span><span class="sxs-lookup"><span data-stu-id="d6630-117">The **XDocuments** collection contains the following methods that can be used for external automation:</span></span> 
  
|<span data-ttu-id="d6630-118">**Method**</span><span class="sxs-lookup"><span data-stu-id="d6630-118">**Method**</span></span>|<span data-ttu-id="d6630-119">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="d6630-119">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="d6630-120">Método **Close**</span><span class="sxs-lookup"><span data-stu-id="d6630-120">**Close** method</span></span>  <br/> |<span data-ttu-id="d6630-121">Fecha o formulário especificado do Microsoft Office InfoPath.</span><span class="sxs-lookup"><span data-stu-id="d6630-121">Closes the specified Microsoft Office InfoPath form.</span></span>  <br/> |
|<span data-ttu-id="d6630-122">**Novo** método</span><span class="sxs-lookup"><span data-stu-id="d6630-122">**New** method</span></span>  <br/> |<span data-ttu-id="d6630-123">Cria um novo formulário do Microsoft Office InfoPath.</span><span class="sxs-lookup"><span data-stu-id="d6630-123">Creates a new Microsoft Office InfoPath form.</span></span>  <br/> |
|<span data-ttu-id="d6630-124">**Método NewFromSolution**</span><span class="sxs-lookup"><span data-stu-id="d6630-124">**NewFromSolution** method</span></span>  <br/> |<span data-ttu-id="d6630-125">Cria um novo formulário do Microsoft Office InfoPath com base no modelo de formulário especificado.</span><span class="sxs-lookup"><span data-stu-id="d6630-125">Creates a new Microsoft Office InfoPath form based on the specified form template.</span></span>  <br/> |
|<span data-ttu-id="d6630-126">**Método NewFromSolutionWithData**</span><span class="sxs-lookup"><span data-stu-id="d6630-126">**NewFromSolutionWithData** method</span></span>  <br/> |<span data-ttu-id="d6630-127">Cria um novo formulário do Microsoft Office InfoPath usando os dados XML especificados e o modelo de formulário.</span><span class="sxs-lookup"><span data-stu-id="d6630-127">Creates a new Microsoft Office InfoPath form using the specified XML data and form template.</span></span>  <br/> |
|<span data-ttu-id="d6630-128">**Método Open**</span><span class="sxs-lookup"><span data-stu-id="d6630-128">**Open** method</span></span>  <br/> |<span data-ttu-id="d6630-129">Abre o formulário especificado do Microsoft Office InfoPath.</span><span class="sxs-lookup"><span data-stu-id="d6630-129">Opens the specified Microsoft Office InfoPath form.</span></span>  <br/> |
   
<span data-ttu-id="d6630-130">Para usar o objeto **Application** de um aplicativo externo, use a função **CreateObject** com o ProgID do aplicativo InfoPath ("InfoPath.Application") para criar uma variável de objeto que representa o aplicativo InfoPath.</span><span class="sxs-lookup"><span data-stu-id="d6630-130">To use the **Application** object from an external application, you use the **CreateObject** function with the ProgID of the InfoPath application ("InfoPath.Application") to create an object variable that represents the InfoPath application.</span></span> <span data-ttu-id="d6630-131">Em seguida, você pode usar a propriedade **XDocuments** para acessar a coleção **XDocuments** e usar seus métodos para abrir ou criar um formulário do InfoPath.</span><span class="sxs-lookup"><span data-stu-id="d6630-131">You can then use the **XDocuments** property to access the **XDocuments** collection and use its methods to open or create an InfoPath form.</span></span> <span data-ttu-id="d6630-132">O exemplo a seguir demonstra a criação de uma referência ao objeto **Application** usando a linguagem de programação microsoft Visual Basic 6.0 ou Visual Basic for Applications (VBA).</span><span class="sxs-lookup"><span data-stu-id="d6630-132">The following example demonstrates the creation of a reference to the **Application** object using the Microsoft Visual Basic 6.0 or Visual Basic for Applications (VBA) programming language:</span></span> 
  
```vb
Dim objIP As Object 
 
Set objIP = CreateObject("InfoPath.Application") 
 
' Open an existing form 
objIP.XDocuments.Open ("C:\MyFolder\MyForm.xml") 
 
' Create a new form based on a form template 
objIP.XDocuments.NewFromSolution ("C:\MyFolder\MyForm.xsn") 

```

> [!NOTE]
> <span data-ttu-id="d6630-133">Como a **função CreateObject** cria uma variável de objeto usando associação tardia, a conclusão automática da instrução não estará disponível no Editor do Visual Basic.</span><span class="sxs-lookup"><span data-stu-id="d6630-133">Because the **CreateObject** function creates an object variable using late binding, automatic statement completion will not be available in the Visual Basic Editor.</span></span> <span data-ttu-id="d6630-134">Consulte os links nas tabelas anteriores para obter informações sobre a sintaxe de chamada correta.</span><span class="sxs-lookup"><span data-stu-id="d6630-134">Refer to the links in the preceding tables for information about the correct calling syntax.</span></span> 
  

