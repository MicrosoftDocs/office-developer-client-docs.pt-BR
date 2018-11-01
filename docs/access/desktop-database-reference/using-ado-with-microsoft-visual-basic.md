---
title: Usando o ADO com o Microsoft Visual Basic
TOCTitle: Using ADO with Microsoft Visual Basic
ms:assetid: 5e0fb2ec-42aa-e181-386f-099607ac7400
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249338(v=office.15)
ms:contentKeyID: 48545130
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 8644bd4f5b1a19848689adf92dca91ba30f324c4
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/31/2018
ms.locfileid: "25889844"
---
# <a name="using-ado-with-microsoft-visual-basic"></a><span data-ttu-id="c07e3-102">Usando o ADO com o Microsoft Visual Basic</span><span class="sxs-lookup"><span data-stu-id="c07e3-102">Using ADO with Microsoft Visual Basic</span></span>


<span data-ttu-id="c07e3-103">**Aplica-se a**: Access 2013, o Office 2013</span><span class="sxs-lookup"><span data-stu-id="c07e3-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="c07e3-p101">A configuração de um projeto ADO e a criação de um código ADO é semelhante quando você usa o Visual Basic ou o Visual Basic for Applications. Este tópico aborda o uso do ADO com o Visual Basic e o Visual Basic for Applications e indica as diferenças.</span><span class="sxs-lookup"><span data-stu-id="c07e3-p101">Setting up an ADO project and writing ADO code is similar whether you use Visual Basic or Visual Basic for Applications. This topic addresses using ADO with both Visual Basic and Visual Basic for Applications and notes any differences.</span></span>

## <a name="referencing-the-ado-library"></a><span data-ttu-id="c07e3-106">Fazendo referência à biblioteca ADO</span><span class="sxs-lookup"><span data-stu-id="c07e3-106">Referencing the ADO Library</span></span>

<span data-ttu-id="c07e3-107">A biblioteca ADO deve ser referenciada pelo seu projeto.</span><span class="sxs-lookup"><span data-stu-id="c07e3-107">The ADO library must be referenced by your project.</span></span>

<span data-ttu-id="c07e3-108">**Para fazer referência ao ADO a partir do Microsoft Visual Basic**</span><span class="sxs-lookup"><span data-stu-id="c07e3-108">**To reference ADO from Microsoft Visual Basic**</span></span>

1.  <span data-ttu-id="c07e3-109">No Visual Basic, no menu **Projeto**, selecione **Referências...**.</span><span class="sxs-lookup"><span data-stu-id="c07e3-109">In Visual Basic, from the **Project** menu, select **References...**.</span></span>

2.  <span data-ttu-id="c07e3-p102">Selecione **Biblioteca Microsoft ActiveX Data Objects x.x** na lista. Verifique se pelo menos as bibliotecas a seguir também estão selecionadas:</span><span class="sxs-lookup"><span data-stu-id="c07e3-p102">Select **Microsoft ActiveX Data Objects x.x Library** from the list. Verify that at least the following libraries are also selected:</span></span>
    
    - <span data-ttu-id="c07e3-112">Visual Basic for Applications</span><span class="sxs-lookup"><span data-stu-id="c07e3-112">Visual Basic for Applications</span></span>
    
    - <span data-ttu-id="c07e3-113">Procedimentos e objetos em tempo de execução do Visual Basic</span><span class="sxs-lookup"><span data-stu-id="c07e3-113">Visual Basic runtime objects and procedures</span></span>
    
    - <span data-ttu-id="c07e3-114">Procedimentos e objetos do Visual Basic</span><span class="sxs-lookup"><span data-stu-id="c07e3-114">Visual Basic objects and procedures</span></span>
    
    - <span data-ttu-id="c07e3-115">Automação OLE</span><span class="sxs-lookup"><span data-stu-id="c07e3-115">OLE Automation</span></span>

3.  <span data-ttu-id="c07e3-116">Clique em **OK**.</span><span class="sxs-lookup"><span data-stu-id="c07e3-116">Click **OK**.</span></span>

<span data-ttu-id="c07e3-117">Você pode usar o ADO facilmente com o Visual Basic for Applications, por meio do Microsoft Access, por exemplo.</span><span class="sxs-lookup"><span data-stu-id="c07e3-117">You can use ADO just as easily with Visual Basic for Applications, using Microsoft Access, for example.</span></span>

<span data-ttu-id="c07e3-118">**Para fazer referência ao ADO a partir do Microsoft Access**</span><span class="sxs-lookup"><span data-stu-id="c07e3-118">**To reference ADO from Microsoft Access**</span></span>

1.  <span data-ttu-id="c07e3-119">No Microsoft Access, selecione ou crie um módulo a partir da guia **Módulos** na janela **Banco de dados**.</span><span class="sxs-lookup"><span data-stu-id="c07e3-119">In Microsoft Access, select or create a module from the **Modules** tab in the **Database** window.</span></span>

2.  <span data-ttu-id="c07e3-120">No menu **Ferramentas**, selecione **Referências...**.</span><span class="sxs-lookup"><span data-stu-id="c07e3-120">From the **Tools** menu, select **References...**.</span></span>

3.  <span data-ttu-id="c07e3-p103">Selecione **Biblioteca Microsoft ActiveX Data Objects x.x** na lista. Verifique se pelo menos as bibliotecas a seguir também estão selecionadas:</span><span class="sxs-lookup"><span data-stu-id="c07e3-p103">Select **Microsoft ActiveX Data Objects x.x Library** from the list. Verify that at least the following libraries are also selected:</span></span>
    
    - <span data-ttu-id="c07e3-123">Visual Basic for Applications</span><span class="sxs-lookup"><span data-stu-id="c07e3-123">Visual Basic for Applications</span></span>
    
    - <span data-ttu-id="c07e3-124">Biblioteca de objetos do Microsoft Access 11.0 (ou posterior)</span><span class="sxs-lookup"><span data-stu-id="c07e3-124">Microsoft Access 11.0 Object Library (or later)</span></span>

4.  <span data-ttu-id="c07e3-125">Clique em **OK**.</span><span class="sxs-lookup"><span data-stu-id="c07e3-125">Click **OK**.</span></span>

## <a name="creating-ado-objects-in-visual-basic"></a><span data-ttu-id="c07e3-126">Criando objetos ADO no Visual Basic</span><span class="sxs-lookup"><span data-stu-id="c07e3-126">Creating ADO Objects in Visual Basic</span></span>

<span data-ttu-id="c07e3-127">Para criar uma variável de automação e uma instância de um objeto para essa variável, você pode usar dois métodos: **Dim** ou **CreateObject**.</span><span class="sxs-lookup"><span data-stu-id="c07e3-127">To create an automation variable and an instance of an object for that variable, you can use two methods: **Dim** or **CreateObject**.</span></span>

## <a name="dim"></a><span data-ttu-id="c07e3-128">Dim</span><span class="sxs-lookup"><span data-stu-id="c07e3-128">Dim</span></span>

<span data-ttu-id="c07e3-129">Use a palavra-chave **New** com **Dim** para declarar e instanciar objetos ADO em uma única etapa:</span><span class="sxs-lookup"><span data-stu-id="c07e3-129">You can use the **New** keyword with **Dim** to declare and instantiate ADO objects in one step:</span></span>

```vb 
 
Dim conn As New ADODB.Connection 
```

<span data-ttu-id="c07e3-130">Opcionalmente, a declaração de instrução **Dim** e a instanciação de objeto também pode ter duas etapas:</span><span class="sxs-lookup"><span data-stu-id="c07e3-130">Alternately, the **Dim** statement declaration and object instantiation can also be two steps:</span></span>

```vb 
 
Dim conn As ADODB.Connection 
Set conn = New ADODB.Connection 
```


> [!NOTE]
> <P><span data-ttu-id="c07e3-131">Ele não é necessário usar explicitamente ADODB progid com a instrução <STRONG>Dim</STRONG> , supondo que você referenciou corretamente a biblioteca ADO em seu projeto.</span><span class="sxs-lookup"><span data-stu-id="c07e3-131">It is not required to explicitly use the ADODB progid with the <STRONG>Dim</STRONG> statement, assuming you have properly referenced the ADO library in your project.</span></span> <span data-ttu-id="c07e3-132">Entretanto, sua utilização garante a ausência de conflitos de nomeação com outras bibliotecas.</span><span class="sxs-lookup"><span data-stu-id="c07e3-132">However, using it ensures that you won't have naming conflicts with other libraries.</span></span></P>



<span data-ttu-id="c07e3-133">Por exemplo, se você incluir referências a ADO e a DAO no mesmo projeto, inclua um qualificador para especificar qual modelo de objeto será usado ao instanciar objetos **Recordset**, como no código a seguir:</span><span class="sxs-lookup"><span data-stu-id="c07e3-133">For example, if you include references to both ADO and DAO in the same project, you should include a qualifier to specify which object model to use when instantiating **Recordset** objects, as in the following code:</span></span>  
<span data-ttu-id="c07e3-134">AdoRS Dim como ADODB. Conjunto de registros</span><span class="sxs-lookup"><span data-stu-id="c07e3-134">Dim adoRS As ADODB.Recordset</span></span>  
  
<span data-ttu-id="c07e3-135">DaoRS Dim como DAO. Conjunto de registros</span><span class="sxs-lookup"><span data-stu-id="c07e3-135">Dim daoRS As DAO.Recordset</span></span>

## <a name="createobject"></a><span data-ttu-id="c07e3-136">CreateObject</span><span class="sxs-lookup"><span data-stu-id="c07e3-136">CreateObject</span></span>

<span data-ttu-id="c07e3-137">Com o método **CreateObject**, a declaração e a instanciação de objeto deverá ter duas etapas separadas:</span><span class="sxs-lookup"><span data-stu-id="c07e3-137">With the **CreateObject** method, the declaration and object instantiation must be two discrete steps:</span></span>

```vb 
 
Dim conn1 
Set conn1 = CreateObject("ADODB.Connection") As Object 
```

<span data-ttu-id="c07e3-p105">Os objetos instanciados com **CreateObject** são acoplados posteriormente, ou seja, eles não são do tipo de alta segurança, e a conclusão da linha de comando estará desabilitada. Entretanto, com ele, você não precisará fazer referência à biblioteca ADO a partir de seu projeto e poderá instanciar versões específicas de objetos. Por exemplo:</span><span class="sxs-lookup"><span data-stu-id="c07e3-p105">Objects instantiated with **CreateObject** are late-bound, which means that they are not strongly typed and command-line completion is disabled. However, it does allow you to skip referencing the ADO library from your project, and enables you to instantiate specific versions of objects. For example:</span></span>

```vb 
 
Set conn1 = CreateObject("ADODB.Connection.2.0") As Object 
```

<span data-ttu-id="c07e3-141">Você também pode fazer isso desenvolvendo uma referência específica à biblioteca de tipos ADO versão 2.0 e criando o objeto.</span><span class="sxs-lookup"><span data-stu-id="c07e3-141">You could also accomplish this by specifically creating a reference to the ADO version 2.0 type library and creating the object.</span></span>

<span data-ttu-id="c07e3-142">A instanciação de objetos com o método **CreateObject** geralmente é mais lenta do que o uso da instrução **Dim**.</span><span class="sxs-lookup"><span data-stu-id="c07e3-142">Instantiating objects with the **CreateObject** method is typically slower than using the **Dim** statement.</span></span>

## <a name="handling-events"></a><span data-ttu-id="c07e3-143">Manipulando eventos</span><span class="sxs-lookup"><span data-stu-id="c07e3-143">Handling Events</span></span>

<span data-ttu-id="c07e3-p106">Para manipular eventos ADO no Microsoft Visual Basic, declare uma variável em nível de módulo usando a palavra-chave **WithEvents**. A variável pode ser declarada apenas como parte de um módulo de classe e deve ser declarada no nível de módulo. Para obter uma discussão mais completa sobre a manipulação de eventos ADO, consulte o [Capítulo 7: Manipulando eventos ADO](chapter-7-handling-ado-events.md).</span><span class="sxs-lookup"><span data-stu-id="c07e3-p106">In order to handle ADO events in Microsoft Visual Basic, you must declare a module-level variable using the **WithEvents** keyword. The variable can be declared only as part of a class module and must be declared at the module level. For a more complete discussion of handling ADO events, see [Chapter 7: Handling ADO Events](chapter-7-handling-ado-events.md).</span></span>

## <a name="visual-basic-examples"></a><span data-ttu-id="c07e3-147">Exemplos de Visual Basic</span><span class="sxs-lookup"><span data-stu-id="c07e3-147">Visual Basic Examples</span></span>

<span data-ttu-id="c07e3-148">Vários exemplos de Visual Basic são incluídos com a documentação do ADO.</span><span class="sxs-lookup"><span data-stu-id="c07e3-148">Many Visual Basic examples are included with the ADO documentation.</span></span> <span data-ttu-id="c07e3-149">Para obter mais informações, consulte [exemplos de código ADO no Microsoft Visual Basic](ado-code-examples-in-microsoft-visual-basic.md).</span><span class="sxs-lookup"><span data-stu-id="c07e3-149">For more information, see [ADO code examples in Microsoft Visual Basic](ado-code-examples-in-microsoft-visual-basic.md).</span></span>

