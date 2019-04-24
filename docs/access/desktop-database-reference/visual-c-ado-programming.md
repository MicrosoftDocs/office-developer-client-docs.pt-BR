---
title: Programação de ADO do Visual C++
TOCTitle: Visual C++ ADO programming
ms:assetid: 117c4fad-8c11-5e3a-ea0c-18811e87475f
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248878(v=office.15)
ms:contentKeyID: 48543319
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 2a890b4906fb9f207f12ff17ef0d3ccf1a97a44d
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32302769"
---
# <a name="visual-c-ado-programming"></a><span data-ttu-id="6478b-102">Programação de ADO do Visual C++</span><span class="sxs-lookup"><span data-stu-id="6478b-102">Visual C++ ADO programming</span></span>

<span data-ttu-id="6478b-103">**Aplica-se ao:** Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="6478b-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="6478b-104">A Referência à API do ADO descreve a funcionalidade da API (Application Programming Interface, Interface de Programação de Aplicativos) utilizando uma sintaxe semelhante ao Microsoft Visual Basic.</span><span class="sxs-lookup"><span data-stu-id="6478b-104">The ADO API Reference describes the functionality of the ADO application programming interface (API) using a syntax similar to Microsoft Visual Basic.</span></span> <span data-ttu-id="6478b-105">Embora o público-alvo seja todos os usuários, os programadores do ADO empregam diferentes idiomas como Visual Basic, Visual C++ (com e sem a diretiva de \*\* \#importação\*\* ) e o Visual J++ (com o pacote de classe do ADO/WFC).</span><span class="sxs-lookup"><span data-stu-id="6478b-105">Though the intended audience is all users, ADO programmers employ diverse languages such as Visual Basic, Visual C++ (with and without the **\#import** directive), and Visual J++ (with the ADO/WFC class package).</span></span>

<span data-ttu-id="6478b-106">Para acomodar essa diversidade, os [Índices de sintaxe do ADO para Visual C++](using-ado-with-microsoft-visual-c.md) fornecem sintaxe específica da linguagem Visual C++ com links para descrições comuns de funcionalidade, parâmetros, comportamentos excepcionais e assim por diante, na Referência à API.</span><span class="sxs-lookup"><span data-stu-id="6478b-106">To accommodate this diversity, the [ADO for Visual C++ Syntax Indexes](using-ado-with-microsoft-visual-c.md) provide Visual C++ language-specific syntax with links to common descriptions of functionality, parameters, exceptional behaviors, and so on, in the API Reference.</span></span>

<span data-ttu-id="6478b-p102">O ADO é implementado com as interfaces COM (Component Object Model). Entretanto, é mais fácil para os programadores trabalhar com o COM em certas linguagens de programação do que em outras. Por exemplo, quase todos os detalhes da utilização do COM são tratados de forma implícita para os programadores do Visual Basic, enquanto os programadores do Visual C++ devem eles mesmos se ater a esses detalhes.</span><span class="sxs-lookup"><span data-stu-id="6478b-p102">ADO is implemented with COM (Component Object Model) interfaces. However, it is easier for programmers to work with COM in certain programming languages than others. For example, nearly all the details of using COM are handled implicitly for Visual Basic programmers, whereas Visual C++ programmers must attend to those details themselves.</span></span>

<span data-ttu-id="6478b-110">As seções a seguir resumem os detalhes de programadores C e C++ usando o ADO e a política de \*\* \#importação\*\* .</span><span class="sxs-lookup"><span data-stu-id="6478b-110">The following sections summarize details for C and C++ programmers using ADO and the **\#import** directive.</span></span> <span data-ttu-id="6478b-111">Ele se concentra nos tipos de dados específicos para COM (**Variant**, **BSTR**e **SafeArray**) e tratamento de erros (\_erro\_com).</span><span class="sxs-lookup"><span data-stu-id="6478b-111">It focuses on data types specific to COM (**Variant**, **BSTR**, and **SafeArray**), and error handling (\_com\_error).</span></span>

## <a name="using-the-import-compiler-directive"></a><span data-ttu-id="6478b-112">Usando a \#diretiva importar compilador</span><span class="sxs-lookup"><span data-stu-id="6478b-112">Using the \#import compiler directive</span></span>

<span data-ttu-id="6478b-113">A diretiva de \*\* \#importação\*\* do compilador do Visual C++ simplifica o trabalho com os métodos e as propriedades do ADO.</span><span class="sxs-lookup"><span data-stu-id="6478b-113">The **\#import** Visual C++ compiler directive simplifies working with the ADO methods and properties.</span></span> <span data-ttu-id="6478b-114">A diretiva tem o nome de um arquivo contendo uma biblioteca de tipo, como ADO .dll (Msado15.dll), e gera arquivos de cabeçalho contendo declarações typedef, ponteiros inteligentes para interfaces e constantes enumeradas.</span><span class="sxs-lookup"><span data-stu-id="6478b-114">The directive takes the name of a file containing a type library, such as the ADO .dll (Msado15.dll), and generates header files containing typedef declarations, smart pointers for interfaces, and enumerated constants.</span></span> <span data-ttu-id="6478b-115">Cada interface é encapsulada, ou agrupada, em uma classe.</span><span class="sxs-lookup"><span data-stu-id="6478b-115">Each interface is encapsulated, or wrapped, in a class.</span></span>

<span data-ttu-id="6478b-p105">Para cada operação dentro de uma classe (isto é, uma chamada de método ou propriedade), há uma declaração para chamar a operação diretamente (isto é, o formato "bruto" da operação) e uma declaração para chamar a operação bruta e lançar um erro COM, se a operação não é executada com sucesso. Se a operação for uma propriedade, haverá uma diretiva de compilador que cria uma sintaxe alternativa para a operação que tem uma sintaxe como a de Visual Basic.</span><span class="sxs-lookup"><span data-stu-id="6478b-p105">For each operation within a class (that is, a method or property call), there is a declaration to call the operation directly (that is, the "raw" form of the operation), and a declaration to call the raw operation and throw a COM error if the operation fails to execute successfully. If the operation is a property, there is usually a compiler directive that creates an alternative syntax for the operation that has syntax like Visual Basic.</span></span>

<span data-ttu-id="6478b-118">As operações que recuperam o valor de uma propriedade têm nomes do formulário, \**Get \* \* \* property*.</span><span class="sxs-lookup"><span data-stu-id="6478b-118">Operations that retrieve the value of a property have names of the form, \**Get\*\*\*Property*.</span></span> <span data-ttu-id="6478b-119">As operações que definem o valor de uma propriedade têm nomes do formulário, \**Put \* \* \* Property*.</span><span class="sxs-lookup"><span data-stu-id="6478b-119">Operations that set the value of a property have names of the form, \**Put\*\*\*Property*.</span></span> <span data-ttu-id="6478b-120">As operações que definem o valor de uma propriedade com um ponteiro para um objeto ADO têm nomes do formulário, \**PutRef \* \* \* Propriedade*.</span><span class="sxs-lookup"><span data-stu-id="6478b-120">Operations that set the value of a property with a pointer to an ADO object have names of the form, \**PutRef\*\*\*Property*.</span></span>

<span data-ttu-id="6478b-121">Você pode obter ou definir uma propriedade chamando estes formatos:</span><span class="sxs-lookup"><span data-stu-id="6478b-121">You can get or set a property with calls of these forms:</span></span>

```vb 
 
variable = objectPtr->GetProperty(); // get property value 
objectPtr->PutProperty(value); // set property value 
objectPtr->PutRefProperty(&value); // set property with object pointer 
```

## <a name="using-property-directives"></a><span data-ttu-id="6478b-122">Usando diretivas de propriedade</span><span class="sxs-lookup"><span data-stu-id="6478b-122">Using property directives</span></span>

<span data-ttu-id="6478b-123">A diretiva de \*\* \_ \_compilador declspec (Property...)\*\* é uma extensão de linguagem C específica da Microsoft que declara uma função usada como uma propriedade para ter uma sintaxe alternativa.</span><span class="sxs-lookup"><span data-stu-id="6478b-123">The **\_\_declspec(property...)** compiler directive is a Microsoft-specific C language extension that declares a function used as a property to have an alternative syntax.</span></span> <span data-ttu-id="6478b-124">Consequentemente, você pode definir ou obter valores de uma propriedade de modo semelhante ao Visual Basic.</span><span class="sxs-lookup"><span data-stu-id="6478b-124">As a result, you can set or get values of a property in a way similar to Visual Basic.</span></span> <span data-ttu-id="6478b-125">Por exemplo, é possível definir e obter uma propriedade desta forma:</span><span class="sxs-lookup"><span data-stu-id="6478b-125">For example, you can set and get a property this way:</span></span>

```vb 
 
objectPtr->property = value; // set property value 
variable = objectPtr->property; // get property value 
```

<span data-ttu-id="6478b-126">Observe que não é necessário codificar:</span><span class="sxs-lookup"><span data-stu-id="6478b-126">Notice you do not have to code:</span></span>

```vb 
 
objectPtr->PutProperty(value); // set property value 
variable = objectPtr->GetProperty; // get property value 
```

<span data-ttu-id="6478b-127">O compilador gerará a chamada de propriedade \*\*Get \*\*\* \*-, **Put**-ou \**PutRef* apropriada com base em qual sintaxe alternativa é declarada e se a propriedade está sendo lida ou gravada.</span><span class="sxs-lookup"><span data-stu-id="6478b-127">The compiler will generate the appropriate \**Get\*\*\*-*, **Put**-, or \**PutRef\*\*\*Property* call based on what alternative syntax is declared and whether the property is being read or written.</span></span>

<span data-ttu-id="6478b-128">A diretiva de \*\* \_ \_compilador declspec (Property...)\*\* só pode declarar **Get**, **Put**ou **Get** e **colocar** a sintaxe alternativa para uma função.</span><span class="sxs-lookup"><span data-stu-id="6478b-128">The **\_\_declspec(property...)** compiler directive can only declare **get**, **put**, or **get** and **put** alternative syntax for a function.</span></span> <span data-ttu-id="6478b-129">As operações somente-leitura têm uma declaração **get**; as operações somente-gravação têm apenas uma declaração **put**; as operações de leitura e gravação têm as declarações **get** e **put**.</span><span class="sxs-lookup"><span data-stu-id="6478b-129">Read-only operations only have a **get** declaration; write-only operations only have a **put** declaration; operations that are both read and write have both **get** and **put** declarations.</span></span>

<span data-ttu-id="6478b-130">Apenas duas declarações são possíveis com essa diretiva; no entanto, cada propriedade pode ter três funções de propriedade: \*\*Get \* \*\*\* Property, \*\*Put \* \* \*\* Property e \*\*PutRef \* \* \*\*.</span><span class="sxs-lookup"><span data-stu-id="6478b-130">Only two declarations are possible with this directive; however, each property may have three property functions: \**Get\*\*\*Property*, \**Put\*\*\*Property*, and \**PutRef\*\*\*Property*.</span></span> <span data-ttu-id="6478b-131">Nesse caso, somente dois formatos de propriedade têm uma sintaxe alternativa.</span><span class="sxs-lookup"><span data-stu-id="6478b-131">In that case, only two forms of the property have the alternative syntax.</span></span>

<span data-ttu-id="6478b-132">Por exemplo, a propriedade **ActiveConnection** do objeto **Command** é declarada com uma sintaxe alternativa para \**Get \* \* \* ActiveConnection* e \**PutRef \* \* \* ActiveConnection*.</span><span class="sxs-lookup"><span data-stu-id="6478b-132">For example, the **Command** object **ActiveConnection** property is declared with an alternative syntax for \**Get\*\*\*ActiveConnection* and \**PutRef\*\*\*ActiveConnection*.</span></span> <span data-ttu-id="6478b-133">A sintaxe **PutRef**- é uma boa opção, porque, na prática, você desejará normalmente colocar um objeto **Connection** de abertura (isto é, um ponteiro do objeto **Connection**) nessa propriedade.</span><span class="sxs-lookup"><span data-stu-id="6478b-133">The **PutRef**- syntax is a good choice because in practice, you will typically want to put an open **Connection** object (that is, a **Connection** object pointer) in this property.</span></span> <span data-ttu-id="6478b-134">Por outro lado, o objeto **Recordset** tem as operações **Get**-, **Put**-e \**PutRef \* \* \* ActiveConnection* , mas nenhuma sintaxe alternativa.</span><span class="sxs-lookup"><span data-stu-id="6478b-134">On the other hand, the **Recordset** object has **Get**-, **Put**-, and \**PutRef\*\*\*ActiveConnection* operations, but no alternative syntax.</span></span>

## <a name="collections-the-getitem-method-and-the-item-property"></a><span data-ttu-id="6478b-135">Coleções, o método GetItem e a propriedade item</span><span class="sxs-lookup"><span data-stu-id="6478b-135">Collections, the GetItem method, and the Item property</span></span>

<span data-ttu-id="6478b-136">O ADO define várias coleções, incluindo **Fields**, **Parameters**, **Properties** e **Errors**.</span><span class="sxs-lookup"><span data-stu-id="6478b-136">ADO defines several collections, including **Fields**, **Parameters**, **Properties**, and **Errors**.</span></span> <span data-ttu-id="6478b-137">No Visual C++, o método **GetItem (***index***)** retorna um membro da coleção.</span><span class="sxs-lookup"><span data-stu-id="6478b-137">In Visual C++, the **GetItem(***index***)** method returns a member of the collection.</span></span> <span data-ttu-id="6478b-138">*Index* é uma **Variant**, o valor que é um índice numérico do membro na coleção ou uma sequência de caracteres contendo o nome do membro.</span><span class="sxs-lookup"><span data-stu-id="6478b-138">*Index* is a **Variant**, the value of which is either a numerical index of the member in the collection, or a string containing the name of the member.</span></span>

<span data-ttu-id="6478b-139">A diretiva de \*\* \_ \_compilador declspec (Property...)\*\* declara a propriedade **Item** como uma sintaxe alternativa para o método **GetItem ()** fundamental de cada coleção.</span><span class="sxs-lookup"><span data-stu-id="6478b-139">The **\_\_declspec(property...)** compiler directive declares the **Item** property as an alternative syntax to each collection's fundamental **GetItem()** method.</span></span> <span data-ttu-id="6478b-140">A sintaxe alternativa usa colchetes e se assemelha à referência de matriz.</span><span class="sxs-lookup"><span data-stu-id="6478b-140">The alternative syntax uses square brackets and looks similar to an array reference.</span></span> <span data-ttu-id="6478b-141">Em geral, os dois formatos se assemelham a:</span><span class="sxs-lookup"><span data-stu-id="6478b-141">In general, the two forms look like the following:</span></span>

```vb
    collectionPtr->GetItem(index); 
    collectionPtr->Item[index]; 
```

<span data-ttu-id="6478b-142">Por exemplo, atribua um valor a um campo de um objeto **Recordset**, chamado ***rs***, derivado da tabela **authors** do banco de dados **pubs**.</span><span class="sxs-lookup"><span data-stu-id="6478b-142">For example, assign a value to a field of a **Recordset** object, named ***rs***, derived from the **authors** table of the **pubs** database.</span></span> <span data-ttu-id="6478b-143">Use a propriedade **Item ()** para acessar o terceiro **campo** da coleção Fields \*\*\*\* do objeto **Recordset** (as coleções são indexadas de zero; suponha que o terceiro campo seja denominado ***\_au fname***).</span><span class="sxs-lookup"><span data-stu-id="6478b-143">Use the **Item()** property to access the third **Field** of the **Recordset** object **Fields** collection (collections are indexed from zero; assume the third field is named ***au\_fname***).</span></span> <span data-ttu-id="6478b-144">Em seguida, chame o método **Value()** no objeto **Field** para atribuir um valor de sequência de caracteres.</span><span class="sxs-lookup"><span data-stu-id="6478b-144">Then call the **Value()** method on the **Field** object to assign a string value.</span></span>

<span data-ttu-id="6478b-145">Isso pode ser expressado no Visual Basic das quatro formas a seguir (as últimas duas são exclusivas para Visual Basic; outras linguagem não têm equivalentes):</span><span class="sxs-lookup"><span data-stu-id="6478b-145">This can be expressed in Visual Basic in the following four ways (the last two forms are unique to Visual Basic; other languages do not have equivalents):</span></span>

```vb 
 
rs.Fields.Item(2).Value = "value" 
rs.Fields.Item("au_fname").Value = "value" 
rs(2) = "value" 
rs!au_fname = "value" 
```

<span data-ttu-id="6478b-146">O equivalente no Visual C++ para a primeira das duas formas acima é:</span><span class="sxs-lookup"><span data-stu-id="6478b-146">The equivalent in Visual C++ to the first two forms above is:</span></span>

```cpp 
 
rs->Fields->GetItem(long(2))->PutValue("value"); 
rs->Fields->GetItem("au_fname")->PutValue("value"); 
```

<span data-ttu-id="6478b-147">\-ou-(a sintaxe alternativa para a propriedade **Value** também é mostrada)</span><span class="sxs-lookup"><span data-stu-id="6478b-147">\-or- (the alternative syntax for the **Value** property is also shown)</span></span>

```cpp 
 
rs->Fields->Item[long(2)]->Value = "value"; 
rs->Fields->Item["au_fname"]->Value = "value"; 
```

## <a name="com-specific-data-types"></a><span data-ttu-id="6478b-148">Tipos de dados específicos COM</span><span class="sxs-lookup"><span data-stu-id="6478b-148">COM-specific data types</span></span>

<span data-ttu-id="6478b-p114">Em geral, qualquer tipo de dados do Visual Basic encontrado na Referência à API do ADO tem um equivalente no Visual C++. Isso inclui tipos de dados padrão, como **unsigned char** para Visual Basic **Byte**, **short** para **Integer** e **long** para **Long**. Consulte os Índices de sintaxe para ver exatamente o que é exigido para operadores de um determinado método ou propriedade.</span><span class="sxs-lookup"><span data-stu-id="6478b-p114">In general, any Visual Basic data type you find in the ADO API Reference has a Visual C++ equivalent. These include standard data types such as **unsigned char** for a Visual Basic **Byte**, **short** for **Integer**, and **long** for **Long**. Look in the Syntax Indexes to see exactly what is required for the operands of a given method or property.</span></span>

<span data-ttu-id="6478b-152">As exceções a essa regra são os tipos de dados específicos para COM: **Variant**, **BSTR** e **SafeArray**.</span><span class="sxs-lookup"><span data-stu-id="6478b-152">The exceptions to this rule are the data types specific to COM: **Variant**, **BSTR**, and **SafeArray**.</span></span>

### <a name="variant"></a><span data-ttu-id="6478b-153">Variant</span><span class="sxs-lookup"><span data-stu-id="6478b-153">Variant</span></span>

<span data-ttu-id="6478b-p115">Uma **Variant** é um tipo de dados estruturado que contém um membro de valor e um membro de tipo de dados. Uma **Variant** pode conter uma ampla quantidade de outros tipos de dados, incluindo outra Variant, BSTR, Boolean, IDispatch ou ponteiro IUnknown, moeda, data etc. O COM também fornece métodos que facilitam a conversão de um tipo de dados para outro.</span><span class="sxs-lookup"><span data-stu-id="6478b-p115">A **Variant** is a structured data type that contains a value member and a data type member. A **Variant** may contain a wide range of other data types including another Variant, BSTR, Boolean, IDispatch or IUnknown pointer, currency, date, and so on. COM also provides methods that make it easy to convert one data type to another.</span></span>

<span data-ttu-id="6478b-157">A \*\* \_classe\_Variant t\*\* encapsula e gerencia o tipo de dados **Variant** .</span><span class="sxs-lookup"><span data-stu-id="6478b-157">The **\_variant\_t** class encapsulates and manages the **Variant** data type.</span></span>

<span data-ttu-id="6478b-158">Quando a referência à API do ADO informa que um método ou operando de propriedade tem um valor, isso normalmente significa que o valor é passado em uma \*\* \_Variant\_t\*\*.</span><span class="sxs-lookup"><span data-stu-id="6478b-158">When the ADO API Reference says a method or property operand takes a value, it usually means the value is passed in a **\_variant\_t**.</span></span>

<span data-ttu-id="6478b-p116">Essa regra é explicitamente verdadeira quando a seção **Parâmetros** nos tópicos da Referência à API do ADO informa que um operador é uma **Variant**. Uma exceção é quando a documentação explicitamente informa que o operador tem um tipo de dados padrão, como **Long** ou **Byte** ou uma enumeração. Outra exceção é quando o operador tem uma **String**.</span><span class="sxs-lookup"><span data-stu-id="6478b-p116">This rule is explicitly true when the **Parameters** section in the topics of the ADO API Reference says an operand is a **Variant**. One exception is when the documentation explicitly says the operand takes a standard data type, such as **Long** or **Byte**, or an enumeration. Another exception is when the operand takes a **String**.</span></span>

### <a name="bstr"></a><span data-ttu-id="6478b-162">BSTR</span><span class="sxs-lookup"><span data-stu-id="6478b-162">BSTR</span></span>

<span data-ttu-id="6478b-p117">Um **BSTR** (**B**asic **STR**ing) é um tipo de dados estruturado que contém uma sequência de caracteres e seu comprimento. O COM fornece métodos para alocar, manipular e liberar **BSTR**.</span><span class="sxs-lookup"><span data-stu-id="6478b-p117">A **BSTR** (**B**asic **STR**ing) is a structured data type that contains a character string and the string's length. COM provides methods to allocate, manipulate, and free a **BSTR**.</span></span>

<span data-ttu-id="6478b-165">A \*\* \_classe\_BSTR t\*\* encapsula e gerencia o tipo de dados **BSTR** .</span><span class="sxs-lookup"><span data-stu-id="6478b-165">The **\_bstr\_t** class encapsulates and manages the **BSTR** data type.</span></span>

<span data-ttu-id="6478b-166">Quando a referência à API do ADO informa que um método ou uma propriedade tem um valor **String** , isso significa que o valor está no formato de um \*\* \_BSTR\_t\*\*.</span><span class="sxs-lookup"><span data-stu-id="6478b-166">When the ADO API Reference says a method or property takes a **String** value, it means the value is in the form of a **\_bstr\_t**.</span></span>

#### <a name="casting-variantt-and-bstrt-classes"></a><span data-ttu-id="6478b-167">Converter \_classes\_Variant t \_e\_BSTR t de conversão</span><span class="sxs-lookup"><span data-stu-id="6478b-167">Casting \_variant\_t and \_bstr\_t classes</span></span>

<span data-ttu-id="6478b-168">Normalmente, não é necessário codificar explicitamente uma \*\* \_Variant\_t\*\* ou \*\* \_BSTR\_t\*\* em um argumento para uma operação.</span><span class="sxs-lookup"><span data-stu-id="6478b-168">Often it is not necessary to explicitly code a **\_variant\_t** or **\_bstr\_t** in an argument to an operation.</span></span> <span data-ttu-id="6478b-169">Se a \*\* \_classe\_Variant t\*\* ou \*\* \_BSTR\_t\*\* tiver um construtor que corresponda ao tipo de dados do argumento, o compilador gerará a \*\* \_variante\_apropriada t\*\* ou \*\* \_ BSTR\_t\*\*.</span><span class="sxs-lookup"><span data-stu-id="6478b-169">If the **\_variant\_t** or **\_bstr\_t** class has a constructor that matches the data type of the argument, then the compiler will generate the appropriate **\_variant\_t** or **\_bstr\_t**.</span></span>

<span data-ttu-id="6478b-170">Entretanto, se o argumento for ambíguo, isto é, o tipo de dados do argumento for correspondente a mais de um construtor, será necessário orientar o argumento com o tipo de dados apropriado para chamar o construtor correto.</span><span class="sxs-lookup"><span data-stu-id="6478b-170">However, if the argument is ambiguous, that is, the argument's data type matches more than one constructor, you must cast the argument with the appropriate data type to invoke the correct constructor.</span></span>

<span data-ttu-id="6478b-171">Por exemplo, a declaração para o método **Recordset::Open** é:</span><span class="sxs-lookup"><span data-stu-id="6478b-171">For example, the declaration for the **Recordset::Open** method is:</span></span>

```vb 
 
 HRESULT Open ( 
 const _variant_t & Source, 
 const _variant_t & ActiveConnection, 
 enum CursorTypeEnum CursorType, 
 enum LockTypeEnum LockType, 
 long Options ); 
```

<span data-ttu-id="6478b-172">O argumento ActiveConnection faz referência a uma \*\* \_\_Variant t\*\*, que você pode codificar como uma cadeia de caracteres de conexão ou um ponteiro para um objeto **Connection** aberto.</span><span class="sxs-lookup"><span data-stu-id="6478b-172">The ActiveConnection argument takes a reference to a **\_variant\_t**, which you may code as a connection string or a pointer to an open **Connection** object.</span></span>

<span data-ttu-id="6478b-173">A \*\* \_variante\_correta t\*\* será construída implicitamente se você passar uma cadeia de caracteres como "DSN = pubs; UID = SA; pwd =;" ou um ponteiro como "(IDispatch \*) pconn".</span><span class="sxs-lookup"><span data-stu-id="6478b-173">The correct **\_variant\_t** will be constructed implicitly if you pass a string such as "DSN=pubs;uid=sa;pwd=;", or a pointer such as "(IDispatch \*) pConn".</span></span>

<span data-ttu-id="6478b-174">Ou você pode codificar explicitamente uma \*\* \_Variant\_t\*\* contendo um ponteiro como "\_Variant\_t ((IDispatch \*) pconn, true)".</span><span class="sxs-lookup"><span data-stu-id="6478b-174">Or you may explicitly code a **\_variant\_t** containing a pointer such as "\_variant\_t((IDispatch \*) pConn, true)".</span></span> <span data-ttu-id="6478b-175">O elenco, (IDispatch \*), resolve a ambigüidade com outro construtor que usa um ponteiro para uma interface IUnknown.</span><span class="sxs-lookup"><span data-stu-id="6478b-175">The cast, (IDispatch \*), resolves the ambiguity with another constructor that takes a pointer to an IUnknown interface.</span></span>

<span data-ttu-id="6478b-p120">Um ponto importante a ser mencionado é que o ADO é uma interface IDispatch. Sempre que um ponteiro para um objeto do ADO for transmitido como uma **Variant**, aquele ponteiro deve ser orientado como um ponteiro para uma interface IDispatch.</span><span class="sxs-lookup"><span data-stu-id="6478b-p120">It is a crucial, though seldom mentioned fact, that ADO is an IDispatch interface. Whenever a pointer to an ADO object must be passed as a **Variant**, that pointer must be cast as a pointer to an IDispatch interface.</span></span>

<span data-ttu-id="6478b-178">O último caso codifica explicitamente o segundo argumento booleano do construtor com seu valor padrão opcional true.</span><span class="sxs-lookup"><span data-stu-id="6478b-178">The last case explicitly codes the second boolean argument of the constructor with its optional, default value of true.</span></span> <span data-ttu-id="6478b-179">Esse argumento faz com que o construtor **Variant** chame o método **AddRef**(), que compensa o ADO chamando automaticamente o \*\* \_método\_Variant t:: Release\*\*() quando o método ou a chamada de Propriedade do ADO é concluída.</span><span class="sxs-lookup"><span data-stu-id="6478b-179">This argument causes the **Variant** constructor to call its **AddRef**() method, which compensates for ADO automatically calling the **\_variant\_t::Release**() method when the ADO method or property call completes.</span></span>

### <a name="safearray"></a><span data-ttu-id="6478b-180">SafeArray</span><span class="sxs-lookup"><span data-stu-id="6478b-180">SafeArray</span></span>

<span data-ttu-id="6478b-p122">**SafeArray** é um tipo de dados estruturado que contém uma matriz de outros tipos de dados. **SafeArray** é chamado *safe* porque contém informações sobre os limites de cada dimensão da matriz e limita o acesso aos elementos da matriz dentro desses limites.</span><span class="sxs-lookup"><span data-stu-id="6478b-p122">A **SafeArray** is a structured data type that contains an array of other data types. A **SafeArray** is called *safe* because it contains information about the bounds of each array dimension, and limits access to array elements within those bounds.</span></span>

<span data-ttu-id="6478b-183">Quando a Referência à API do ADO informa que um método ou uma propriedade tem ou retorna uma matriz, isso significa que o método ou a propriedade tem ou retorna **SafeArray**, não uma matriz C/C++ nativa.</span><span class="sxs-lookup"><span data-stu-id="6478b-183">When the ADO API Reference says a method or property takes or returns an array, it means the method or property takes or returns a **SafeArray**, not a native C/C++ array.</span></span>

<span data-ttu-id="6478b-p123">Por exemplo, o segundo parâmetro do método **OpenSchema** do objeto **Connection** requer uma matriz de valores **Variant**. Esses valores **Variant** devem ser transmitidos como elementos de **SafeArray**, e esse **SafeArray** deve ser definido como o valor de outra **Variant**. Isso significa que outra **Variant** é transmitida como o segundo argumento de **OpenSchema**.</span><span class="sxs-lookup"><span data-stu-id="6478b-p123">For example, the second parameter of the **Connection** object **OpenSchema** method requires an array of **Variant** values. Those **Variant** values must be passed as elements of a **SafeArray**, and that **SafeArray** must be set as the value of another **Variant**. It is that other **Variant** that is passed as the second argument of **OpenSchema**.</span></span>

<span data-ttu-id="6478b-187">Como exemplos adicionais, o primeiro argumento do método **Find** é uma **Variant** cujo valor é um **SafeArray** com uma dimensão; cada um dos argumentos principal e secundário opcionais de **AddNew** é um **SafeArray** com uma dimensão; e o valor de retorno do método **GetRows** é uma **Variant** cujo valor é um **SafeArray** com duas dimensões.</span><span class="sxs-lookup"><span data-stu-id="6478b-187">As further examples, the first argument of the **Find** method is a **Variant** whose value is a one-dimensional **SafeArray**; each of the optional first and second arguments of **AddNew** is a one-dimensional **SafeArray**; and the return value of the **GetRows** method is a **Variant** whose value is a two-dimensional **SafeArray**.</span></span>

## <a name="missing-and-default-parameters"></a><span data-ttu-id="6478b-188">Parâmetros ausentes e padrão</span><span class="sxs-lookup"><span data-stu-id="6478b-188">Missing and default parameters</span></span>

<span data-ttu-id="6478b-p124">O Visual Basic permite parâmetros Missing nos métodos. Por exemplo, o método **Open** do objeto **Recordset** tem cinco parâmetros, mas você pode ignorar os parâmetros intermediários e excluir os parâmetros à direita. Um **BSTR** ou **Variant** padrão será substituído dependendo do tipo de dados do operador ausente.</span><span class="sxs-lookup"><span data-stu-id="6478b-p124">Visual Basic allows missing parameters in methods. For example, the **Recordset** object **Open** method has five parameters, but you can skip intermediate parameters and leave off trailing parameters. A default **BSTR** or **Variant** will be substituted depending on the data type of the missing operand.</span></span>

<span data-ttu-id="6478b-192">Em C/C++, todos os operadores devem ser especificados.</span><span class="sxs-lookup"><span data-stu-id="6478b-192">In C/C++, all operands must be specified.</span></span> <span data-ttu-id="6478b-193">Se você quiser especificar um parâmetro ausente cujo tipo de dados é uma cadeia de caracteres, especifique um \*\* \_BSTR\_t\*\* contendo uma cadeia de caracteres nula.</span><span class="sxs-lookup"><span data-stu-id="6478b-193">If you want to specify a missing parameter whose data type is a string, specify a **\_bstr\_t** containing a null string.</span></span> <span data-ttu-id="6478b-194">Se você quiser especificar um parâmetro ausente cujo tipo de dados é uma **Variant**, especifique uma \*\* \_Variant\_t\*\* com um valor de DISP\_e\_PARAMNOTFOUND e um tipo de erro\_VT.</span><span class="sxs-lookup"><span data-stu-id="6478b-194">If you want to specify a missing parameter whose data type is a **Variant**, specify a **\_variant\_t** with a value of DISP\_E\_PARAMNOTFOUND and a type of VT\_ERROR.</span></span> <span data-ttu-id="6478b-195">Como alternativa, especifique a \*\* \_Variant\_t\*\* constante equivalente, **vtMissing**, que é fornecida pela diretiva \*\* \#Import\*\* .</span><span class="sxs-lookup"><span data-stu-id="6478b-195">Alternatively, specify the equivalent **\_variant\_t** constant, **vtMissing**, which is supplied by the **\#import** directive.</span></span>

<span data-ttu-id="6478b-p126">Três métodos são exceções ao uso típico de **vtMissing**. Eles são os métodos **Execute** dos objetos **Connection** e **Command**, e os métodos **NextRecordset** do objeto **Recordset**. A seguir estão suas assinaturas:</span><span class="sxs-lookup"><span data-stu-id="6478b-p126">Three methods are exceptions to the typical use of **vtMissing**. These are the **Execute** methods of the **Connection** and **Command** objects, and the **NextRecordset** method of the **Recordset** object. The following are their signatures:</span></span>

```vb 
 
_RecordsetPtr Invalid DDUE based on source, error:link not allowed in code, link filename:mdmthcnnexecute_HV10294345.xml( _bstr_t CommandText, VARIANT * RecordsAffected, 
 long Options ); // Connection 
_RecordsetPtr Invalid DDUE based on source, error:link not allowed in code, link filename:mdmthcmdexecute_HV10294344.xml( VARIANT * RecordsAffected, VARIANT * Parameters, 
 long Options ); // Command 
_RecordsetPtr Invalid DDUE based on source, error:link not allowed in code, link filename:mdmthnextrec_HV10294541.xml( VARIANT * RecordsAffected ); // Recordset 
```

<span data-ttu-id="6478b-p127">Os parâmetros *RecordsAffected* e *Parameters* são ponteiros para uma **Variant**. *Parameters* é um parâmetro de entrada que especifica o endereço de uma **Variant** contendo um único parâmetro, ou uma matriz de parâmetros, que modifica o comando que está sendo executado. *RecordsAffected* é um parâmetro de saída que especifica o endereço de uma **Variant**, em que o número de linhas afetadas pelo método é retornado.</span><span class="sxs-lookup"><span data-stu-id="6478b-p127">The parameters, *RecordsAffected* and *Parameters*, are pointers to a **Variant**. *Parameters* is an input parameter which specifies the address of a **Variant** containing a single parameter, or array of parameters, that will modify the command being executed. *RecordsAffected* is an output parameter that specifies the address of a **Variant**, where the number of rows affected by the method is returned.</span></span>

<span data-ttu-id="6478b-202">No método **executar** do objeto **Command** , indique que nenhum parâmetro é especificado pela \*\* configuração dos \&parâmetros para vtMissing (que é recomendado) ou para o ponteiro nulo (ou seja, **nulo** ou zero (0)).</span><span class="sxs-lookup"><span data-stu-id="6478b-202">In the **Command** object **Execute** method, indicate that no parameters are specified by setting *Parameters* to either \&vtMissing (which is recommended) or to the null pointer (that is, **NULL** or zero (0)).</span></span> <span data-ttu-id="6478b-203">Se *Parameters* for definido como ponteiro nulo, o método substitui internamente o equivalente a **vtMissing** e, em seguida, conclui a operação.</span><span class="sxs-lookup"><span data-stu-id="6478b-203">If *Parameters* is set to the null pointer, the method internally substitutes the equivalent of **vtMissing**, and then completes the operation.</span></span>

<span data-ttu-id="6478b-p129">Em todos os métodos, indique que o número de registros afetados não deve ser retornado pela definição de *RecordsAffected* como ponteiro nulo. Nesse caso, o ponteiro nulo não é mais um parâmetro Missing nem sequer uma indicação de que o método deve descartar o número de registros afetados.</span><span class="sxs-lookup"><span data-stu-id="6478b-p129">In all the methods, indicate that the number of records affected should not be returned by setting *RecordsAffected* to the null pointer. In this case, the null pointer is not so much a missing parameter as an indication that the method should discard the number of records affected.</span></span>

<span data-ttu-id="6478b-206">Dessa forma, para esses três métodos, é válido codificar algo como:</span><span class="sxs-lookup"><span data-stu-id="6478b-206">Thus, for these three methods, it is valid to code something such as:</span></span>

```vb 
 
pConnection->Execute("commandText", NULL, adCmdText); 
pCommand->Execute(NULL, NULL, adCmdText); 
pRecordset->NextRecordset(NULL); 
```

## <a name="error-handling"></a><span data-ttu-id="6478b-207">Tratamento de erros</span><span class="sxs-lookup"><span data-stu-id="6478b-207">Error handling</span></span>

<span data-ttu-id="6478b-208">No COM, a maioria das operações retornam um código de retorno HRESULT que indica que uma função foi concluída com sucesso.</span><span class="sxs-lookup"><span data-stu-id="6478b-208">In COM, most operations return an HRESULT return code that indicates whether a function completed successfully.</span></span> <span data-ttu-id="6478b-209">A política de \*\* \#importação\*\* gera código de wrapper ao redor de cada método ou propriedade "RAW" e verifica o HRESULT retornado.</span><span class="sxs-lookup"><span data-stu-id="6478b-209">The **\#import** directive generates wrapper code around each "raw" method or property and checks the returned HRESULT.</span></span> <span data-ttu-id="6478b-210">Se o HRESULT indicar falha, o código de wrapper gerará um erro COM \_chamando\_o\_problema com errorex () com o código de retorno HRESULT como um argumento.</span><span class="sxs-lookup"><span data-stu-id="6478b-210">If the HRESULT indicates failure, the wrapper code throws a COM error by calling \_com\_issue\_errorex() with the HRESULT return code as an argument.</span></span> <span data-ttu-id="6478b-211">Os objetos de erro do COM podem ser capturados em um bloco **try**-**catch**.</span><span class="sxs-lookup"><span data-stu-id="6478b-211">COM error objects can be caught in a **try**-**catch** block.</span></span> <span data-ttu-id="6478b-212">(Para fins de eficiência, Capture uma referência a um \*\* \_objeto\_Error com\*\* .)</span><span class="sxs-lookup"><span data-stu-id="6478b-212">(For efficiency's sake, catch a reference to a **\_com\_error** object.)</span></span>

<span data-ttu-id="6478b-p131">Lembre-se, esses são os erros do ADO: eles resultam de falha em operações do ADO. Os erros retornados pelo provedor subjacente aparecem como objetos **Error** na coleção **Errors** do objeto **Connection**.</span><span class="sxs-lookup"><span data-stu-id="6478b-p131">Remember, these are ADO errors: they result from the ADO operation failing. Errors returned by the underlying provider appear as **Error** objects in the **Connection** object **Errors** collection.</span></span>

<span data-ttu-id="6478b-215">A política de \*\* \#importação\*\* cria apenas rotinas de tratamento de erros para métodos e propriedades declaradas no ADO. dll.</span><span class="sxs-lookup"><span data-stu-id="6478b-215">The **\#import** directive creates only error handling routines for methods and properties declared in the ADO .dll.</span></span> <span data-ttu-id="6478b-216">Contudo, você pode aproveitar esse mesmo mecanismo de tratamento de erros escrevendo sua própria macro de verificação de erros ou sua função inline.</span><span class="sxs-lookup"><span data-stu-id="6478b-216">However, you can take advantage of this same error handling mechanism by writing your own error checking macro or inline function.</span></span> <span data-ttu-id="6478b-217">Consulte o tópico [Extensões do Visual C++](visual-c-extensions-for-ado.md) ou o código nas seções a seguir para obter exemplos.</span><span class="sxs-lookup"><span data-stu-id="6478b-217">See the topic, [Visual C++ Extensions](visual-c-extensions-for-ado.md), or the code in the following sections for examples.</span></span>

## <a name="visual-c-equivalents-of-visual-basic-conventions"></a><span data-ttu-id="6478b-218">Equivalentes do Visual C++ das convenções do Visual Basic</span><span class="sxs-lookup"><span data-stu-id="6478b-218">Visual C++ equivalents of Visual Basic conventions</span></span>

<span data-ttu-id="6478b-219">A seguir está um resumo de várias convenções na documentação do ADO, codificadas no Visual Basic, bem como seus equivalentes no Visual C++.</span><span class="sxs-lookup"><span data-stu-id="6478b-219">The following is a summary of several conventions in the ADO documentation, coded in Visual Basic, as well as their equivalents in Visual C++.</span></span>

### <a name="declaring-an-ado-object"></a><span data-ttu-id="6478b-220">Declarar um objeto ADO</span><span class="sxs-lookup"><span data-stu-id="6478b-220">Declaring an ADO object</span></span>

<span data-ttu-id="6478b-221">No Visual Basic, uma variável de objeto do ADO (nesse caso para um objeto **Recordset** ) é declarada como se segue:</span><span class="sxs-lookup"><span data-stu-id="6478b-221">In Visual Basic, an ADO object variable (in this case for a **Recordset** object) is declared as follows:</span></span>

```vb 
 
Dim rst As ADODB.Recordset 
```

<span data-ttu-id="6478b-222">A cláusula "ADODB. Recordset ", é o ProgID do objeto **Recordset** , conforme definido no registro.</span><span class="sxs-lookup"><span data-stu-id="6478b-222">The clause, "ADODB.Recordset", is the ProgID of the **Recordset** object as defined in the Registry.</span></span> <span data-ttu-id="6478b-223">Uma nova instância de um objeto **Record** é declarado como a seguir:</span><span class="sxs-lookup"><span data-stu-id="6478b-223">A new instance of a **Record** object is declared as follows:</span></span>

```vb 
 
Dim rst As New ADODB.Recordset 
```

<span data-ttu-id="6478b-224">\-ou</span><span class="sxs-lookup"><span data-stu-id="6478b-224">\-or-</span></span>

```vb 
 
Dim rst As ADODB.Recordset 
Set rst = New ADODB.Recordset 
```

<span data-ttu-id="6478b-225">No Visual C++, a diretiva de \*\* \#importação\*\* gera declarações de tipo de ponteiro inteligente para todos os objetos ADO.</span><span class="sxs-lookup"><span data-stu-id="6478b-225">In Visual C++, the **\#import** directive generates smart pointer-type declarations for all the ADO objects.</span></span> <span data-ttu-id="6478b-226">Por exemplo, uma variável que aponta para um \*\* \_objeto Recordset\*\* é do tipo \*\* \_RecordsetPtr\*\*e é declarada da seguinte maneira:</span><span class="sxs-lookup"><span data-stu-id="6478b-226">For example, a variable that points to a **\_Recordset** object is of type **\_RecordsetPtr**, and is declared as follows:</span></span>

```cpp 
 
_RecordsetPtr rs; 
```

<span data-ttu-id="6478b-227">Uma variável que aponta para uma nova instância de um \*\* \_objeto Recordset\*\* é declarada da seguinte maneira:</span><span class="sxs-lookup"><span data-stu-id="6478b-227">A variable that points to a new instance of a **\_Recordset** object is declared as follows:</span></span>

```cpp 
 
_RecordsetPtr rs("ADODB.Recordset"); 
```

<span data-ttu-id="6478b-228">\-ou</span><span class="sxs-lookup"><span data-stu-id="6478b-228">\-or-</span></span>

```cpp 
 
_RecordsetPtr rs; 
rs.CreateInstance("ADODB.Recordset"); 
```

<span data-ttu-id="6478b-229">\-ou</span><span class="sxs-lookup"><span data-stu-id="6478b-229">\-or-</span></span>

```cpp 
 
_RecordsetPtr rs; 
rs.CreateInstance(__uuidof(_Recordset)); 
```

<span data-ttu-id="6478b-230">Depois que o método **CreateInstance** é chamado, a variável pode ser utilizada como se segue:</span><span class="sxs-lookup"><span data-stu-id="6478b-230">After the **CreateInstance** method is called, the variable can be used as follows:</span></span>

```cpp 
 
rs->Open(...); 
```

<span data-ttu-id="6478b-231">Observe que, em um caso, o operador "." é usado como se a variável fosse uma instância de uma classe (RS. CreateInstance) e, em outro caso, o operador "\>-" é usado como se a variável fosse um ponteiro para uma interface (RS-\>Open).</span><span class="sxs-lookup"><span data-stu-id="6478b-231">Notice that in one case, the "." operator is used as if the variable were an instance of a class (rs.CreateInstance), and in another case, the "-\>" operator is used as if the variable were a pointer to an interface (rs-\>Open).</span></span>

<span data-ttu-id="6478b-232">Uma variável pode ser usada de duas maneiras porque o operador "\>-" está sobrecarregado para permitir que uma instância de uma classe se comporte como um ponteiro para uma interface.</span><span class="sxs-lookup"><span data-stu-id="6478b-232">One variable can be used in two ways because the "-\>" operator is overloaded to allow an instance of a class to behave like a pointer to an interface.</span></span> <span data-ttu-id="6478b-233">Um membro de classe privada da variável de instância contém um ponteiro para \*\* \_\*\* a interface Recordset; o operador "\>-" retorna esse ponteiro; e o ponteiro retornado acessa os membros do objeto \*\* \_Recordset\*\* .</span><span class="sxs-lookup"><span data-stu-id="6478b-233">A private class member of the instance variable contains a pointer to the **\_Recordset** interface; the "-\>" operator returns that pointer; and the returned pointer accesses the members of the **\_Recordset** object.</span></span>

### <a name="coding-a-missing-parameter"></a><span data-ttu-id="6478b-234">Codificando um parâmetro ausente</span><span class="sxs-lookup"><span data-stu-id="6478b-234">Coding a missing parameter</span></span>

#### <a name="string"></a><span data-ttu-id="6478b-235">String</span><span class="sxs-lookup"><span data-stu-id="6478b-235">String</span></span>

<span data-ttu-id="6478b-236">Quando é necessário codificar um operador **String** ausente no Visual Basic, você simplesmente omite o operador.</span><span class="sxs-lookup"><span data-stu-id="6478b-236">When you need to code a missing **String** operand in Visual Basic, you merely omit the operand.</span></span> <span data-ttu-id="6478b-237">Você deve especificar o operador no Visual C++.</span><span class="sxs-lookup"><span data-stu-id="6478b-237">You must specify the operand in Visual C++.</span></span> <span data-ttu-id="6478b-238">Código um \*\* \_BSTR\_t\*\* que tem uma cadeia de caracteres vazia como um valor.</span><span class="sxs-lookup"><span data-stu-id="6478b-238">Code a **\_bstr\_t** that has an empty string as a value.</span></span>

```cpp 
 
_bstr_t strMissing(L""); 
```

#### <a name="variant"></a><span data-ttu-id="6478b-239">Variant</span><span class="sxs-lookup"><span data-stu-id="6478b-239">Variant</span></span>

<span data-ttu-id="6478b-240">Quando é necessário codificar um operador **Variant** ausente no Visual Basic, você simplesmente omite o operador.</span><span class="sxs-lookup"><span data-stu-id="6478b-240">When you need to code a missing **Variant** operand in Visual Basic, you merely omit the operand.</span></span> <span data-ttu-id="6478b-241">Você deve especificar todos os operadores no Visual C++.</span><span class="sxs-lookup"><span data-stu-id="6478b-241">You must specify all operands in Visual C++.</span></span> <span data-ttu-id="6478b-242">Código um parâmetro **Variant** ausente com uma \*\* \_Variant\_t\*\* definida como o valor especial,\_a\_PARAMNOTFOUND e o tipo, o erro\_VT.</span><span class="sxs-lookup"><span data-stu-id="6478b-242">Code a missing **Variant** parameter with a **\_variant\_t** set to the special value, DISP\_E\_PARAMNOTFOUND, and type, VT\_ERROR.</span></span> <span data-ttu-id="6478b-243">Como alternativa, especifique **vtMissing**, que é uma constante predefinida equivalente fornecida pela diretiva \*\* \#Import\*\* .</span><span class="sxs-lookup"><span data-stu-id="6478b-243">Alternatively, specify **vtMissing**, which is an equivalent pre-defined constant supplied by the **\#import** directive.</span></span>

```cpp 
 
_variant_t vtMissingYours(DISP_E_PARAMNOTFOUND, VT_ERROR); 
```

<span data-ttu-id="6478b-244">\-ou use-</span><span class="sxs-lookup"><span data-stu-id="6478b-244">\-or use -</span></span>

```cpp 
 
...vtMissing...; 
```

### <a name="declaring-a-variant"></a><span data-ttu-id="6478b-245">Declarar uma Variant</span><span class="sxs-lookup"><span data-stu-id="6478b-245">Declaring a variant</span></span>

<span data-ttu-id="6478b-246">No Visual Basic, uma **Variant** é declarada como a instrução **Dim** como se segue:</span><span class="sxs-lookup"><span data-stu-id="6478b-246">In Visual Basic, a **Variant** is declared with the **Dim** statement as follows:</span></span>

```vb 
 
Dim VariableName As Variant 
```

<span data-ttu-id="6478b-247">No Visual C++, declare uma variável como tipo \*\* \_Variant\_t\*\*.</span><span class="sxs-lookup"><span data-stu-id="6478b-247">In Visual C++, declare a variable as type **\_variant\_t**.</span></span> <span data-ttu-id="6478b-248">Algumas declarações de \*\* \_variante\_de variantes t\*\* são mostradas abaixo.</span><span class="sxs-lookup"><span data-stu-id="6478b-248">A few schematic **\_variant\_t** declarations are shown below.</span></span>

> [!NOTE]
> <span data-ttu-id="6478b-p139">[!OBSERVAçãO] Essas declarações fornecem uma pequena ideia do que você codificaria em seu próprio programa. Para obter mais informações, consulte os exemplos abaixo e a documentação do Visual C++.</span><span class="sxs-lookup"><span data-stu-id="6478b-p139">These declarations merely give a rough idea of what you would code in your own program. For more information, see the examples below, and the Visual C++ documentation.</span></span>

```cpp 
 
_variant_t VariableName(value); 
_variant_t VariableName((data type cast) value); 
_variant_t VariableName(value, VT_DATATYPE); 
_variant_t VariableName(interface * value, bool fAddRef = true); 
```

### <a name="using-arrays-of-variants"></a><span data-ttu-id="6478b-251">Usando matrizes de variantes</span><span class="sxs-lookup"><span data-stu-id="6478b-251">Using arrays of variants</span></span>

<span data-ttu-id="6478b-252">No Visual Basic, as matrizes de **Variants** podem ser codificadas com a instrução **Dim** ou podem utilizar a função **Array**, como demonstrado no seguinte código de exemplo:</span><span class="sxs-lookup"><span data-stu-id="6478b-252">In Visual Basic, arrays of **Variants** can be coded with the **Dim** statement, or you may use the **Array** function, as demonstrated in the following example code:</span></span>

```vb 
 
Public Sub ArrayOfVariants 
Dim cn As ADODB.Connection 
Dim rs As ADODB.Recordset 
Dim fld As ADODB.Field 
 
cn.Open "DSN=pubs", "sa", "" 
rs = cn.OpenSchema(adSchemaColumns, _ 
 Array(Empty, Empty, "authors", Empty)) 
For Each fld in rs.Fields 
 Debug.Print "Name = "; fld.Name 
Next fld 
rs.Close 
cn.Close 
End Sub 
```

<span data-ttu-id="6478b-253">O seguinte exemplo do Visual C++ demonstra o uso de **SafeArray** usado com uma \*\* \_Variant\_t\*\*.</span><span class="sxs-lookup"><span data-stu-id="6478b-253">The following Visual C++ example demonstrates using a **SafeArray** used with a **\_variant\_t**.</span></span>

> [!NOTE]
> <span data-ttu-id="6478b-254">As seguintes notas correspondem às seções comentadas no exemplo de código.</span><span class="sxs-lookup"><span data-stu-id="6478b-254">The following notes correspond to commented sections in the code example.</span></span>

1. <span data-ttu-id="6478b-255">Novamente, a função inline TESTHR() é definida para aproveitar a existência do mecanismo de tratamento de erros.</span><span class="sxs-lookup"><span data-stu-id="6478b-255">Once again, the TESTHR() inline function is defined to take advantage of the existing error-handling mechanism.</span></span>

2. <span data-ttu-id="6478b-p140">Você precisa apenas de uma matriz com uma dimensão para poder utilizar **SafeArrayCreateVector**, em vez da declaração **SAFEARRAYBOUND** e da função **SafeArrayCreate** de objetivos gerais. A seguir está um exemplo de como o código é, usando **SafeArrayCreate**:</span><span class="sxs-lookup"><span data-stu-id="6478b-p140">You only need a one-dimensional array, so you can use **SafeArrayCreateVector**, instead of the general purpose **SAFEARRAYBOUND** declaration and **SafeArrayCreate** function. The following is what that code would look like using **SafeArrayCreate**:</span></span>
    
   ```cpp 
     
     SAFEARRAYBOUND sabound[1]; 
     sabound[0].lLbound = 0; 
     sabound[0].cElements = 4; 
     pSa = SafeArrayCreate(VT_VARIANT, 1, sabound); 
   ```

3. <span data-ttu-id="6478b-258">O esquema identificado pela constante enumerada, **adSchemaColumns**, é associado a quatro colunas de restrição: catálogo\_de tabelas,\_esquema de tabela\_, nome da tabela\_e nome da coluna.</span><span class="sxs-lookup"><span data-stu-id="6478b-258">The schema identified by the enumerated constant, **adSchemaColumns**, is associated with four constraint columns: TABLE\_CATALOG, TABLE\_SCHEMA, TABLE\_NAME, and COLUMN\_NAME.</span></span> <span data-ttu-id="6478b-259">Portanto, uma matriz de valores **Variant** com quatro elementos é criada.</span><span class="sxs-lookup"><span data-stu-id="6478b-259">Therefore, an array of **Variant** values with four elements is created.</span></span> <span data-ttu-id="6478b-260">Em seguida, um valor de restrição que corresponde à terceira coluna\_, nome de tabela, é especificado.</span><span class="sxs-lookup"><span data-stu-id="6478b-260">Then a constraint value that corresponds to the third column, TABLE\_NAME, is specified.</span></span> <span data-ttu-id="6478b-261">O **Recordset** retornado consiste em várias colunas, um subconjunto de colunas de restrição.</span><span class="sxs-lookup"><span data-stu-id="6478b-261">The **Recordset** that is returned consists of several columns, a subset of which is the constraint columns.</span></span> <span data-ttu-id="6478b-262">Os valores das colunas de restrição para cada linha retornada deve ser igual aos valores de restrição correspondentes.</span><span class="sxs-lookup"><span data-stu-id="6478b-262">The values of the constraint columns for each returned row must be the same as the corresponding constraint values.</span></span>

4. <span data-ttu-id="6478b-263">Aqueles que conhecem o **SafeArrays** podem ficar surpresos, pois o **SafeArrayDestroy**() não é chamado antes da saída.</span><span class="sxs-lookup"><span data-stu-id="6478b-263">Those familiar with **SafeArrays** may be surprised that **SafeArrayDestroy**() is not called before the exit.</span></span> <span data-ttu-id="6478b-264">Na verdade, chamar **SafeArrayDestroy**() nesse caso causará uma exceção de tempo de execução.</span><span class="sxs-lookup"><span data-stu-id="6478b-264">In fact, calling **SafeArrayDestroy**() in this case will cause a run-time exception.</span></span> <span data-ttu-id="6478b-265">O motivo é que o destruidor para vtCriteria chamará **VariantClear**() quando a \*\* \_Variant\_t\*\* sair do escopo, que liberará a **SafeArray**.</span><span class="sxs-lookup"><span data-stu-id="6478b-265">The reason is that the destructor for vtCriteria will call **VariantClear**() when the **\_variant\_t** goes out of scope, which will free the **SafeArray**.</span></span> <span data-ttu-id="6478b-266">Chamar **SafeArrayDestroy**, sem limpar manualmente a \*\* \_Variant\_t\*\*, faria com que o destruidor tentasse limpar um ponteiro **SafeArray** inválido.</span><span class="sxs-lookup"><span data-stu-id="6478b-266">Calling **SafeArrayDestroy**, without manually clearing the **\_variant\_t**, would cause the destructor to try to clear an invalid **SafeArray** pointer.</span></span> <span data-ttu-id="6478b-267">Se **SafeArrayDestroy** for chamado, o código será parecido com:</span><span class="sxs-lookup"><span data-stu-id="6478b-267">If **SafeArrayDestroy** were called, the code would look like this:</span></span>
    
   ```cpp 
     
     TESTHR(SafeArrayDestroy(pSa)); 
     vtCriteria.vt = VT_EMPTY; 
     vtCriteria.parray = NULL; 
   ```
    
   <span data-ttu-id="6478b-268">No entanto, é muito mais simples permitir que \*\* \_a\_Variant t\*\* gerencie **SafeArray**.</span><span class="sxs-lookup"><span data-stu-id="6478b-268">However, it is much simpler to let the **\_variant\_t** manage the **SafeArray**.</span></span>


```cpp 
 
    #import "c:\Program Files\Common Files\System\ADO\msado15.dll" no_namespace rename("EOF", "EndOfFile") 
    #include <stdio.h> 
    
    // Note 1 
    inline void TESTHR( HRESULT _hr ) 
    { if FAILED(_hr) _com_issue_error(_hr); } 
    
    void main(void) 
    { 
    CoInitialize(NULL); 
    try 
    { 
    _RecordsetPtr pRs("ADODB.Recordset"); 
    _ConnectionPtr pCn("ADODB.Connection"); 
    _variant_t vtTableName("authors"), 
    vtCriteria; 
    long ix[1]; 
    SAFEARRAY *pSa = NULL; 
    
    pCn->Open("DSN=pubs;User ID=MyUserId;pwd=MyPassword;Provider=MSDASQL;", "", "", 
    adConnectUnspecified); 
    // Note 2, Note 3 
    pSa = SafeArrayCreateVector(VT_VARIANT, 1, 4); 
    if (!pSa) _com_issue_error(E_OUTOFMEMORY); 
    
    // Specify TABLE_NAME in the third array element (index of 2). 
    
    ix[0] = 2; 
    TESTHR(SafeArrayPutElement(pSa, ix, &vtTableName)); 
    
    // There is no Variant constructor for a SafeArray, so manually set the 
    // type (SafeArray of Variant) and value (pointer to a SafeArray). 
    
    vtCriteria.vt = VT_ARRAY | VT_VARIANT; 
    vtCriteria.parray = pSa; 
    
    pRs = pCn->OpenSchema(adSchemaColumns, vtCriteria, vtMissing); 
    
    long limit = pRs->GetFields()->Count; 
    for (long x = 0; x < limit; x++) 
    printf("%d: %s\n", x+1, 
    ((char*) pRs->GetFields()->Item[x]->Name)); 
    // Note 4 
    pRs->Close(); 
    pCn->Close(); 
    } 
    catch (_com_error &e) 
    { 
    printf("Error:\n"); 
    printf("Code = %08lx\n", e.Error()); 
    printf("Code meaning = %s\n", (char*) e.ErrorMessage()); 
    printf("Source = %s\n", (char*) e.Source()); 
    printf("Description = %s\n", (char*) e.Description()); 
    } 
    CoUninitialize(); 
    } 
```

### <a name="using-property-getputputref"></a><span data-ttu-id="6478b-269">Usando a propriedade Get/Put/PutRef</span><span class="sxs-lookup"><span data-stu-id="6478b-269">Using property Get/Put/PutRef</span></span>

<span data-ttu-id="6478b-270">No Visual Basic, o nome de uma propriedade não é qualificado se ela for recuperada, atribuída ou atribuída a uma referência.</span><span class="sxs-lookup"><span data-stu-id="6478b-270">In Visual Basic, the name of a property is not qualified by whether it is retrieved, assigned, or assigned a reference.</span></span>

```vb
    Public Sub GetPutPutRef 
    Dim rs As New ADODB.Recordset 
    Dim cn As New ADODB.Connection 
    Dim sz as Integer 
    cn.Open "Provider=sqloledb;Data Source=yourserver;" & _ 
     "Initial Catalog=pubs;Integrated Security=SSPI;" 
    rs.PageSize = 10 
    sz = rs.PageSize 
    rs.ActiveConnection = cn 
    rs.Open "authors",,adOpenStatic 
    ' ... 
    rs.Close 
    cn.Close 
    End Sub
```

<span data-ttu-id="6478b-271">Este exemplo do Visual C++ demonstra a propriedade **Get**/**Put**/\*\*PutRef \* \*\*\*.</span><span class="sxs-lookup"><span data-stu-id="6478b-271">This Visual C++ example demonstrates the **Get**/**Put**/\**PutRef\*\*\*Property*.</span></span>

> [!NOTE]
> <span data-ttu-id="6478b-272">[!OBSERVAçãO] As seguintes notas correspondem às seções comentadas no exemplo de código.</span><span class="sxs-lookup"><span data-stu-id="6478b-272">The following notes correspond to commented sections in the code example.</span></span>

1. <span data-ttu-id="6478b-273">Este exemplo usa duas formas de um argumento de cadeia de caracteres ausente: uma constante explícita, **strMissing**, e uma cadeia de caracteres que o compilador usará para criar um valor de \*\* \_BSTR\_\*\* temporário que existirá para o escopo do método **Open** .</span><span class="sxs-lookup"><span data-stu-id="6478b-273">This example uses two forms of a missing string argument: an explicit constant, **strMissing**, and a string that the compiler will use to create a temporary **\_bstr\_t** that will exist for the scope of the **Open** method.</span></span>

2. <span data-ttu-id="6478b-274">Não é necessário converter o operando do RS-\>PutRefActiveConnection (CN) em (IDispatch \*) porque o tipo do operando já é (IDispatch \*).</span><span class="sxs-lookup"><span data-stu-id="6478b-274">It isn't necessary to cast the operand of rs-\>PutRefActiveConnection(cn) to (IDispatch \*) because the type of the operand is already (IDispatch \*).</span></span>
    
   ```cpp 
     
    #import "c:\Program Files\Common Files\System\ADO\msado15.dll" no_namespace rename("EOF", "EndOfFile") 
    #include <stdio.h> 
     
    void main(void) 
    { 
     CoInitialize(NULL); 
     try 
     { 
     _ConnectionPtr cn("ADODB.Connection"); 
     _RecordsetPtr rs("ADODB.Recordset"); 
     _bstr_t strMissing(L""); 
     long oldPgSz = 0, 
     newPgSz = 5; 
     
    // Note 1 
     cn->Open("Provider=sqloledb;Data Source=MyServer;" 
     "Initial Catalog=pubs;Integrated Security=SSPI;", 
     strMissing, "", 
     adConnectUnspecified); 
     
     oldPgSz = rs->GetPageSize(); 
     // -or- 
     oldPgSz = rs->PageSize; 
     
     rs->PutPageSize(newPgSz); 
     // -or- 
     rs->PageSize = newPgSz; 
     
    // Note 2 
     rs->PutRefActiveConnection( cn ); 
     rs->Open("authors", vtMissing, adOpenStatic, adLockReadOnly, 
     adCmdTable); 
     printf("Original pagesize = %d, new pagesize = %d\n", oldPgSz, 
     rs->GetPageSize()); 
     rs->Close(); 
     cn->Close(); 
     } 
     catch (_com_error &e) 
     { 
     printf("Description = %s\n", (char*) e.Description()); 
     } 
     ::CoUninitialize(); 
    } 
   ```

### <a name="using-getitemx-and-itemx"></a><span data-ttu-id="6478b-275">Usando GetItem (x) e item\[x\]</span><span class="sxs-lookup"><span data-stu-id="6478b-275">Using GetItem(x) and Item\[x\]</span></span>

<span data-ttu-id="6478b-276">Esse exemplo do Visual Basic demonstra a sintaxe padrão e alternativa para **Item**().</span><span class="sxs-lookup"><span data-stu-id="6478b-276">This Visual Basic example demonstrates the standard and alternative syntax for **Item**().</span></span>

```vb 
 
Public Sub GetItemItem 
Dim rs As New ADODB.Recordset 
Dim name as String 
rs = rs.Open "authors", "DSN=pubs;", adOpenDynamic, _ 
 adLockBatchOptimistic, adTable 
name = rs(0) 
' -or- 
name = rs.Fields.Item(0) 
rs(0) = "Test" 
rs.UpdateBatch 
' Restore name 
rs(0) = name 
rs.UpdateBatch 
rs.Close 
End Sub 
```

<span data-ttu-id="6478b-277">Esse exemplo do Visual C++ demonstra **Item**.</span><span class="sxs-lookup"><span data-stu-id="6478b-277">This Visual C++ example demonstrates **Item**.</span></span>

> [!NOTE]
> <span data-ttu-id="6478b-278">[!OBSERVAçãO] A seguinte nota corresponde às seções comentadas no exemplo de código.</span><span class="sxs-lookup"><span data-stu-id="6478b-278">The following note corresponds to commented sections in the code example.</span></span>

1. <span data-ttu-id="6478b-279">Quando a coleção é acessada com **Item**, o índice **2** deve ser orientado para **long** para que um construtor apropriado seja chamado.</span><span class="sxs-lookup"><span data-stu-id="6478b-279">When the collection is accessed with **Item**, the index, **2**, must be cast to **long** so an appropriate constructor will be invoked.</span></span>
    
   ```cpp 
     
    #import "c:\Program Files\Common Files\System\ADO\msado15.dll" no_namespace rename("EOF", "EndOfFile") 
    #include <stdio.h> 
     
    void main(void) 
    { 
     CoInitialize(NULL); 
     try { 
     _RecordsetPtr rs("ADODB.Recordset"); 
     _variant_t vtFirstName; 
     
     rs->Open("authors", 
     "Provider=sqloledb;Data Source=MyServer;" 
     "Initial Catalog=pubs;Integrated Security=SSPI;", 
     adOpenStatic, adLockOptimistic, adCmdTable); 
     rs->MoveFirst(); 
     
    // Note 1. Get a field. 
     vtFirstName = rs->Fields->GetItem((long)2)->GetValue(); 
     // -or- 
     vtFirstName = rs->Fields->Item[(long)2]->Value; 
     
     printf( "First name = '%s'\n", (char*) ((_bstr_t) vtFirstName)); 
     
     rs->Fields->GetItem((long)2)->Value = L"TEST"; 
     rs->Update(vtMissing, vtMissing); 
     
     // Restore name 
     rs->Fields->GetItem((long)2)->PutValue(vtFirstName); 
     // -or- 
     rs->Fields->GetItem((long)2)->Value = vtFirstName; 
     rs->Update(vtMissing, vtMissing); 
     rs->Close(); 
     } 
     catch (_com_error &e) 
     { 
     printf("Description = '%s'\n", (char*) e.Description()); 
     } 
     ::CoUninitialize(); 
    } 
   ```

### <a name="casting-ado-object-pointers-with-idispatch-"></a><span data-ttu-id="6478b-280">Orientando ponteiros de objeto do ADO com (IDispatch \*)</span><span class="sxs-lookup"><span data-stu-id="6478b-280">Casting ADO object pointers with (IDispatch \*)</span></span>

<span data-ttu-id="6478b-281">O seguinte exemplo do Visual C++ demonstra o uso de (IDispatch \*) para orientar ponteiros de objetos do ADO.</span><span class="sxs-lookup"><span data-stu-id="6478b-281">The following Visual C++ example demonstrates using (IDispatch \*) to cast ADO object pointers.</span></span>

> [!NOTE]
> <span data-ttu-id="6478b-282">[!OBSERVAçãO] As seguintes notas correspondem às seções comentadas no exemplo de código.</span><span class="sxs-lookup"><span data-stu-id="6478b-282">The following notes correspond to commented sections in the code example.</span></span>

1. <span data-ttu-id="6478b-283">Especifique um objeto **Connection** de abertura em uma **Variant** explicitamente codificada.</span><span class="sxs-lookup"><span data-stu-id="6478b-283">Specify an open **Connection** object in an explicitly coded **Variant**.</span></span> <span data-ttu-id="6478b-284">ConVertê-lo com \*(IDispatch) para que o Construtor correto seja invocado.</span><span class="sxs-lookup"><span data-stu-id="6478b-284">Cast it with (IDispatch \*) so the correct constructor will be invoked.</span></span> <span data-ttu-id="6478b-285">Além disso, defina explicitamente o segundo \*\*\*\* \*\* \_parâmetro de Variant\_t\*\* como o valor padrão de true, de modo que a contagem de referência do objeto estará correta quando a operação **Recordset:: Open** terminar.</span><span class="sxs-lookup"><span data-stu-id="6478b-285">Also, explicitly set the second **\_variant\_t** parameter to the default value of **true**, so the object reference count will be correct when the **Recordset::Open** operation ends.</span></span>

2. <span data-ttu-id="6478b-286">A expressão, (\_BSTR\_t), não é uma conversão, mas um \*\* \_operador\_Variant t\*\* que extrai uma \*\*\*\* \*\*\*\* \*\* \_cadeia de\_caracteres BSTR t\*\* da variante retornada por value.</span><span class="sxs-lookup"><span data-stu-id="6478b-286">The expression, (\_bstr\_t), is not a cast, but a **\_variant\_t** operator that extracts a **\_bstr\_t** string from the **Variant** returned by **Value**.</span></span> <span data-ttu-id="6478b-287">A expressão, (Char\*), não é uma conversão, mas um operador de \*\* \_t de\_BSTR\*\* que extrai um ponteiro para a cadeia de caracteres encapsulada em um \*\* \_objeto BSTR\_t\*\* .</span><span class="sxs-lookup"><span data-stu-id="6478b-287">The expression, (char\*), is not a cast, but a **\_bstr\_t** operator that extracts a pointer to the encapsulated string in a **\_bstr\_t** object.</span></span> <span data-ttu-id="6478b-288">Esta seção de código demonstra alguns dos comportamentos úteis dos \*\* \_operadores Variant\_t\*\* e \*\* \_BSTR\_t\*\* .</span><span class="sxs-lookup"><span data-stu-id="6478b-288">This section of code demonstrates some of the useful behaviors of **\_variant\_t** and **\_bstr\_t** operators.</span></span>
    
   ```cpp 
     
    #import "c:\Program Files\Common Files\System\ADO\msado15.dll" no_namespace rename("EOF", "EndOfFile") 
     
    #include <stdio.h> 
     
    void main(void) 
    { 
     CoInitialize(NULL); 
     try 
     { 
     _ConnectionPtr pConn("ADODB.Connection"); 
     _RecordsetPtr pRst("ADODB.Recordset"); 
     
     pConn->Open("Provider=sqloledb;Data Source=MyServer;" 
     "Initial Catalog=pubs;Integrated Security=SSPI;", 
     "", "", adConnectUnspecified); 
    // Note 1. 
     pRst->Open( 
     "authors", 
     _variant_t((IDispatch *) pConn, true), 
     adOpenStatic, 
     adLockReadOnly, 
     adCmdTable); 
     pRst->MoveLast(); 
    // Note 2. 
     printf("Last name is '%s %s'\n", 
     (char*) ((_bstr_t) pRst->GetFields()->GetItem("au_fname")->GetValue()), 
     (char*) ((_bstr_t) pRst->Fields->Item["au_lname"]->Value)); 
     
     pRst->Close(); 
     pConn->Close(); 
     } 
     catch (_com_error &e) 
     { 
     printf("Description = '%s'\n", (char*) e.Description()); 
     } 
    ::CoUninitialize(); 
    } 
   ```

