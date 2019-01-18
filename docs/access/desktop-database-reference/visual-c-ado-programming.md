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
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: pt-BR
ms.lasthandoff: 01/17/2019
ms.locfileid: "28721287"
---
# <a name="visual-c-ado-programming"></a><span data-ttu-id="eb1ec-102">Programação de ADO do Visual C++</span><span class="sxs-lookup"><span data-stu-id="eb1ec-102">Visual C++ ADO programming</span></span>

<span data-ttu-id="eb1ec-103">**Aplica-se a**: Access 2013, o Office 2013</span><span class="sxs-lookup"><span data-stu-id="eb1ec-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="eb1ec-104">A Referência à API do ADO descreve a funcionalidade da API (Application Programming Interface, Interface de Programação de Aplicativos) utilizando uma sintaxe semelhante ao Microsoft Visual Basic.</span><span class="sxs-lookup"><span data-stu-id="eb1ec-104">The ADO API Reference describes the functionality of the ADO application programming interface (API) using a syntax similar to Microsoft Visual Basic.</span></span> <span data-ttu-id="eb1ec-105">Embora o público-alvo esteja todos os usuários, programadores ADO empregam diversos idiomas, como o Visual Basic, Visual C++ (com e sem o \*\* \#importar\*\* diretiva) e Visual J++ (com o pacote de classe ADO/WFC).</span><span class="sxs-lookup"><span data-stu-id="eb1ec-105">Though the intended audience is all users, ADO programmers employ diverse languages such as Visual Basic, Visual C++ (with and without the **\#import** directive), and Visual J++ (with the ADO/WFC class package).</span></span>

<span data-ttu-id="eb1ec-106">Para acomodar essa diversidade, os [Índices de sintaxe do ADO para Visual C++](using-ado-with-microsoft-visual-c.md) fornecem sintaxe específica da linguagem Visual C++ com links para descrições comuns de funcionalidade, parâmetros, comportamentos excepcionais e assim por diante, na Referência à API.</span><span class="sxs-lookup"><span data-stu-id="eb1ec-106">To accommodate this diversity, the [ADO for Visual C++ Syntax Indexes](using-ado-with-microsoft-visual-c.md) provide Visual C++ language-specific syntax with links to common descriptions of functionality, parameters, exceptional behaviors, and so on, in the API Reference.</span></span>

<span data-ttu-id="eb1ec-p102">O ADO é implementado com as interfaces COM (Component Object Model). Entretanto, é mais fácil para os programadores trabalhar com o COM em certas linguagens de programação do que em outras. Por exemplo, quase todos os detalhes da utilização do COM são tratados de forma implícita para os programadores do Visual Basic, enquanto os programadores do Visual C++ devem eles mesmos se ater a esses detalhes.</span><span class="sxs-lookup"><span data-stu-id="eb1ec-p102">ADO is implemented with COM (Component Object Model) interfaces. However, it is easier for programmers to work with COM in certain programming languages than others. For example, nearly all the details of using COM are handled implicitly for Visual Basic programmers, whereas Visual C++ programmers must attend to those details themselves.</span></span>

<span data-ttu-id="eb1ec-110">As seções a seguir resumem os detalhes para programadores C e C++ usando o ADO e o \*\* \#importar\*\* diretiva.</span><span class="sxs-lookup"><span data-stu-id="eb1ec-110">The following sections summarize details for C and C++ programmers using ADO and the **\#import** directive.</span></span> <span data-ttu-id="eb1ec-111">Ela se concentra em tipos de dados específicos do COM (**Variant**, **BSTR**e **SafeArray**) e tratamento de erros (\_com\_erro).</span><span class="sxs-lookup"><span data-stu-id="eb1ec-111">It focuses on data types specific to COM (**Variant**, **BSTR**, and **SafeArray**), and error handling (\_com\_error).</span></span>

## <a name="using-the-import-compiler-directive"></a><span data-ttu-id="eb1ec-112">Usando o \#importar a diretiva de compilador</span><span class="sxs-lookup"><span data-stu-id="eb1ec-112">Using the \#import compiler directive</span></span>

<span data-ttu-id="eb1ec-113">O \*\* \#importar\*\* diretiva de compilador do Visual C++ simplifica o trabalho com as propriedades e métodos do ADO.</span><span class="sxs-lookup"><span data-stu-id="eb1ec-113">The **\#import** Visual C++ compiler directive simplifies working with the ADO methods and properties.</span></span> <span data-ttu-id="eb1ec-114">A diretiva tem o nome de um arquivo contendo uma biblioteca de tipo, como ADO .dll (Msado15.dll), e gera arquivos de cabeçalho contendo declarações typedef, ponteiros inteligentes para interfaces e constantes enumeradas.</span><span class="sxs-lookup"><span data-stu-id="eb1ec-114">The directive takes the name of a file containing a type library, such as the ADO .dll (Msado15.dll), and generates header files containing typedef declarations, smart pointers for interfaces, and enumerated constants.</span></span> <span data-ttu-id="eb1ec-115">Cada interface é encapsulada, ou agrupada, em uma classe.</span><span class="sxs-lookup"><span data-stu-id="eb1ec-115">Each interface is encapsulated, or wrapped, in a class.</span></span>

<span data-ttu-id="eb1ec-p105">Para cada operação dentro de uma classe (isto é, uma chamada de método ou propriedade), há uma declaração para chamar a operação diretamente (isto é, o formato "bruto" da operação) e uma declaração para chamar a operação bruta e lançar um erro COM, se a operação não é executada com sucesso. Se a operação for uma propriedade, haverá uma diretiva de compilador que cria uma sintaxe alternativa para a operação que tem uma sintaxe como a de Visual Basic.</span><span class="sxs-lookup"><span data-stu-id="eb1ec-p105">For each operation within a class (that is, a method or property call), there is a declaration to call the operation directly (that is, the "raw" form of the operation), and a declaration to call the raw operation and throw a COM error if the operation fails to execute successfully. If the operation is a property, there is usually a compiler directive that creates an alternative syntax for the operation that has syntax like Visual Basic.</span></span>

<span data-ttu-id="eb1ec-118">Operações que recuperar o valor de uma propriedade têm nomes do formulário, \**obter \* \* \* propriedade*.</span><span class="sxs-lookup"><span data-stu-id="eb1ec-118">Operations that retrieve the value of a property have names of the form, \**Get\*\*\*Property*.</span></span> <span data-ttu-id="eb1ec-119">Operações que defina o valor de uma propriedade têm nomes do formulário, \**colocar \* \* \* propriedade*.</span><span class="sxs-lookup"><span data-stu-id="eb1ec-119">Operations that set the value of a property have names of the form, \**Put\*\*\*Property*.</span></span> <span data-ttu-id="eb1ec-120">Operações que defina o valor de uma propriedade com um ponteiro para um objeto ADO têm nomes do formulário, \**PutRef \* \* \* propriedade*.</span><span class="sxs-lookup"><span data-stu-id="eb1ec-120">Operations that set the value of a property with a pointer to an ADO object have names of the form, \**PutRef\*\*\*Property*.</span></span>

<span data-ttu-id="eb1ec-121">Você pode obter ou definir uma propriedade chamando estes formatos:</span><span class="sxs-lookup"><span data-stu-id="eb1ec-121">You can get or set a property with calls of these forms:</span></span>

```vb 
 
variable = objectPtr->GetProperty(); // get property value 
objectPtr->PutProperty(value); // set property value 
objectPtr->PutRefProperty(&value); // set property with object pointer 
```

## <a name="using-property-directives"></a><span data-ttu-id="eb1ec-122">Utilizando diretivas de propriedade</span><span class="sxs-lookup"><span data-stu-id="eb1ec-122">Using property directives</span></span>

<span data-ttu-id="eb1ec-123">O \*\* \_ \_declspec(property...)\*\* diretiva de compilador é uma extensão de idioma específico do Microsoft C declara uma função usada como uma propriedade para ter uma sintaxe alternativa.</span><span class="sxs-lookup"><span data-stu-id="eb1ec-123">The **\_\_declspec(property...)** compiler directive is a Microsoft-specific C language extension that declares a function used as a property to have an alternative syntax.</span></span> <span data-ttu-id="eb1ec-124">Consequentemente, você pode definir ou obter valores de uma propriedade de modo semelhante ao Visual Basic.</span><span class="sxs-lookup"><span data-stu-id="eb1ec-124">As a result, you can set or get values of a property in a way similar to Visual Basic.</span></span> <span data-ttu-id="eb1ec-125">Por exemplo, é possível definir e obter uma propriedade desta forma:</span><span class="sxs-lookup"><span data-stu-id="eb1ec-125">For example, you can set and get a property this way:</span></span>

```vb 
 
objectPtr->property = value; // set property value 
variable = objectPtr->property; // get property value 
```

<span data-ttu-id="eb1ec-126">Observe que não é necessário codificar:</span><span class="sxs-lookup"><span data-stu-id="eb1ec-126">Notice you do not have to code:</span></span>

```vb 
 
objectPtr->PutProperty(value); // set property value 
variable = objectPtr->GetProperty; // get property value 
```

<span data-ttu-id="eb1ec-127">O compilador irá gerar apropriada \*\*Get \* \* *-*, **Coloque**-, ou \**PutRef \* \* \* propriedade* chamada com base na sintaxe alternativa declarada e se a propriedade está sendo lidos ou gravados.</span><span class="sxs-lookup"><span data-stu-id="eb1ec-127">The compiler will generate the appropriate \**Get\*\*\*-*, **Put**-, or \**PutRef\*\*\*Property* call based on what alternative syntax is declared and whether the property is being read or written.</span></span>

<span data-ttu-id="eb1ec-128">O \*\* \_ \_declspec(property...)\*\* diretiva de compilador só pode declarar **obter**, **colocar**ou **obtêm** ou **colocam** sintaxe alternativa para uma função.</span><span class="sxs-lookup"><span data-stu-id="eb1ec-128">The **\_\_declspec(property...)** compiler directive can only declare **get**, **put**, or **get** and **put** alternative syntax for a function.</span></span> <span data-ttu-id="eb1ec-129">As operações somente-leitura têm uma declaração **get**; as operações somente-gravação têm apenas uma declaração **put**; as operações de leitura e gravação têm as declarações **get** e **put**.</span><span class="sxs-lookup"><span data-stu-id="eb1ec-129">Read-only operations only have a **get** declaration; write-only operations only have a **put** declaration; operations that are both read and write have both **get** and **put** declarations.</span></span>

<span data-ttu-id="eb1ec-130">Apenas duas declarações são possíveis com essa diretiva; No entanto, cada propriedade pode ter três funções de propriedade: \**obter \* \* \* propriedade*, \**colocar \* \* \* propriedade*, e \**PutRef \* \* \* propriedade*.</span><span class="sxs-lookup"><span data-stu-id="eb1ec-130">Only two declarations are possible with this directive; however, each property may have three property functions: \**Get\*\*\*Property*, \**Put\*\*\*Property*, and \**PutRef\*\*\*Property*.</span></span> <span data-ttu-id="eb1ec-131">Nesse caso, somente dois formatos de propriedade têm uma sintaxe alternativa.</span><span class="sxs-lookup"><span data-stu-id="eb1ec-131">In that case, only two forms of the property have the alternative syntax.</span></span>

<span data-ttu-id="eb1ec-132">Por exemplo, o propriedade **ActiveConnection** do objeto **Command** é declarado como uma sintaxe alternativa para \**obter \* \* \* ActiveConnection* e \**PutRef \* \* \* ActiveConnection*.</span><span class="sxs-lookup"><span data-stu-id="eb1ec-132">For example, the **Command** object **ActiveConnection** property is declared with an alternative syntax for \**Get\*\*\*ActiveConnection* and \**PutRef\*\*\*ActiveConnection*.</span></span> <span data-ttu-id="eb1ec-133">O **PutRef**- sintaxe é uma boa opção porque prática, será conveniente colocar um objeto de **Conexão** (ou seja, um indicador de objeto de **Conexão** ) aberto nessa propriedade normalmente.</span><span class="sxs-lookup"><span data-stu-id="eb1ec-133">The **PutRef**- syntax is a good choice because in practice, you will typically want to put an open **Connection** object (that is, a **Connection** object pointer) in this property.</span></span> <span data-ttu-id="eb1ec-134">Por outro lado, o objeto **Recordset** tem **Get**-, **Coloque**-, e \**PutRef \* \* \* ActiveConnection* operações, mas nenhuma sintaxe alternativa.</span><span class="sxs-lookup"><span data-stu-id="eb1ec-134">On the other hand, the **Recordset** object has **Get**-, **Put**-, and \**PutRef\*\*\*ActiveConnection* operations, but no alternative syntax.</span></span>

## <a name="collections-the-getitem-method-and-the-item-property"></a><span data-ttu-id="eb1ec-135">Coleções, o método GetItem e a propriedade Item</span><span class="sxs-lookup"><span data-stu-id="eb1ec-135">Collections, the GetItem method, and the Item property</span></span>

<span data-ttu-id="eb1ec-p111">O ADO define várias coleções, incluindo **Fields**, **Parameters**, **Properties** e **Errors**. No Visual C++, o método **GetItem(***index***)** retorna um membro da coleção. *Index* é uma **Variant**, o valor que é um índice numérico do membro na coleção ou uma sequência de caracteres contendo o nome do membro.</span><span class="sxs-lookup"><span data-stu-id="eb1ec-p111">ADO defines several collections, including **Fields**, **Parameters**, **Properties**, and **Errors**. In Visual C++, the **GetItem(***index***)** method returns a member of the collection. *Index* is a **Variant**, the value of which is either a numerical index of the member in the collection, or a string containing the name of the member.</span></span>

<span data-ttu-id="eb1ec-139">O \*\* \_ \_declspec(property...)\*\* diretiva de compilador declara a propriedade **Item** como uma sintaxe alternativa ao método de **obter GetItem ()** fundamental da cada coleção.</span><span class="sxs-lookup"><span data-stu-id="eb1ec-139">The **\_\_declspec(property...)** compiler directive declares the **Item** property as an alternative syntax to each collection's fundamental **GetItem()** method.</span></span> <span data-ttu-id="eb1ec-140">A sintaxe alternativa usa colchetes e se assemelha à referência de matriz.</span><span class="sxs-lookup"><span data-stu-id="eb1ec-140">The alternative syntax uses square brackets and looks similar to an array reference.</span></span> <span data-ttu-id="eb1ec-141">Em geral, os dois formatos se assemelham a:</span><span class="sxs-lookup"><span data-stu-id="eb1ec-141">In general, the two forms look like the following:</span></span>

```vb
    collectionPtr->GetItem(index); 
    collectionPtr->Item[index]; 
```

<span data-ttu-id="eb1ec-142">Por exemplo, atribua um valor a um campo de um objeto **Recordset** , chamado ***rs***, derivado da tabela **authors** de banco de dados **pubs** .</span><span class="sxs-lookup"><span data-stu-id="eb1ec-142">For example, assign a value to a field of a **Recordset** object, named ***rs***, derived from the **authors** table of the **pubs** database.</span></span> <span data-ttu-id="eb1ec-143">Use a propriedade de **item ()** para acessar o terceiro **campo** do objeto **Recordset** a coleção **Fields** (coleções são indexadas a partir de zero; assume o terceiro campo é chamado ***au\_fname***).</span><span class="sxs-lookup"><span data-stu-id="eb1ec-143">Use the **Item()** property to access the third **Field** of the **Recordset** object **Fields** collection (collections are indexed from zero; assume the third field is named ***au\_fname***).</span></span> <span data-ttu-id="eb1ec-144">Em seguida, chame o método **Value()** no objeto **Field** para atribuir um valor de sequência de caracteres.</span><span class="sxs-lookup"><span data-stu-id="eb1ec-144">Then call the **Value()** method on the **Field** object to assign a string value.</span></span>

<span data-ttu-id="eb1ec-145">Isso pode ser expressado no Visual Basic das quatro formas a seguir (as últimas duas são exclusivas para Visual Basic; outras linguagem não têm equivalentes):</span><span class="sxs-lookup"><span data-stu-id="eb1ec-145">This can be expressed in Visual Basic in the following four ways (the last two forms are unique to Visual Basic; other languages do not have equivalents):</span></span>

```vb 
 
rs.Fields.Item(2).Value = "value" 
rs.Fields.Item("au_fname").Value = "value" 
rs(2) = "value" 
rs!au_fname = "value" 
```

<span data-ttu-id="eb1ec-146">O equivalente no Visual C++ para a primeira das duas formas acima é:</span><span class="sxs-lookup"><span data-stu-id="eb1ec-146">The equivalent in Visual C++ to the first two forms above is:</span></span>

```cpp 
 
rs->Fields->GetItem(long(2))->PutValue("value"); 
rs->Fields->GetItem("au_fname")->PutValue("value"); 
```

<span data-ttu-id="eb1ec-147">\-ou -(a sintaxe alternativa para a propriedade **Value** também é mostrada)</span><span class="sxs-lookup"><span data-stu-id="eb1ec-147">\-or- (the alternative syntax for the **Value** property is also shown)</span></span>

```cpp 
 
rs->Fields->Item[long(2)]->Value = "value"; 
rs->Fields->Item["au_fname"]->Value = "value"; 
```

## <a name="com-specific-data-types"></a><span data-ttu-id="eb1ec-148">Tipos de dados específicos do COM</span><span class="sxs-lookup"><span data-stu-id="eb1ec-148">COM-specific data types</span></span>

<span data-ttu-id="eb1ec-p114">Em geral, qualquer tipo de dados do Visual Basic encontrado na Referência à API do ADO tem um equivalente no Visual C++. Isso inclui tipos de dados padrão, como **unsigned char** para Visual Basic **Byte**, **short** para **Integer** e **long** para **Long**. Consulte os Índices de sintaxe para ver exatamente o que é exigido para operadores de um determinado método ou propriedade.</span><span class="sxs-lookup"><span data-stu-id="eb1ec-p114">In general, any Visual Basic data type you find in the ADO API Reference has a Visual C++ equivalent. These include standard data types such as **unsigned char** for a Visual Basic **Byte**, **short** for **Integer**, and **long** for **Long**. Look in the Syntax Indexes to see exactly what is required for the operands of a given method or property.</span></span>

<span data-ttu-id="eb1ec-152">As exceções a essa regra são os tipos de dados específicos para COM: **Variant**, **BSTR** e **SafeArray**.</span><span class="sxs-lookup"><span data-stu-id="eb1ec-152">The exceptions to this rule are the data types specific to COM: **Variant**, **BSTR**, and **SafeArray**.</span></span>

### <a name="variant"></a><span data-ttu-id="eb1ec-153">Variant</span><span class="sxs-lookup"><span data-stu-id="eb1ec-153">Variant</span></span>

<span data-ttu-id="eb1ec-p115">Uma **Variant** é um tipo de dados estruturado que contém um membro de valor e um membro de tipo de dados. Uma **Variant** pode conter uma ampla quantidade de outros tipos de dados, incluindo outra Variant, BSTR, Boolean, IDispatch ou ponteiro IUnknown, moeda, data etc. O COM também fornece métodos que facilitam a conversão de um tipo de dados para outro.</span><span class="sxs-lookup"><span data-stu-id="eb1ec-p115">A **Variant** is a structured data type that contains a value member and a data type member. A **Variant** may contain a wide range of other data types including another Variant, BSTR, Boolean, IDispatch or IUnknown pointer, currency, date, and so on. COM also provides methods that make it easy to convert one data type to another.</span></span>

<span data-ttu-id="eb1ec-157">O \*\* \_variant\_t\*\* classe encapsula e gerencia o tipo de dados **Variant** .</span><span class="sxs-lookup"><span data-stu-id="eb1ec-157">The **\_variant\_t** class encapsulates and manages the **Variant** data type.</span></span>

<span data-ttu-id="eb1ec-158">Quando a referência de API do ADO informa que um método ou propriedade tem um valor, isso normalmente significa que o valor é transmitido em uma \*\* \_variant\_t\*\*.</span><span class="sxs-lookup"><span data-stu-id="eb1ec-158">When the ADO API Reference says a method or property operand takes a value, it usually means the value is passed in a **\_variant\_t**.</span></span>

<span data-ttu-id="eb1ec-p116">Essa regra é explicitamente verdadeira quando a seção **Parâmetros** nos tópicos da Referência à API do ADO informa que um operador é uma **Variant**. Uma exceção é quando a documentação explicitamente informa que o operador tem um tipo de dados padrão, como **Long** ou **Byte** ou uma enumeração. Outra exceção é quando o operador tem uma **String**.</span><span class="sxs-lookup"><span data-stu-id="eb1ec-p116">This rule is explicitly true when the **Parameters** section in the topics of the ADO API Reference says an operand is a **Variant**. One exception is when the documentation explicitly says the operand takes a standard data type, such as **Long** or **Byte**, or an enumeration. Another exception is when the operand takes a **String**.</span></span>

### <a name="bstr"></a><span data-ttu-id="eb1ec-162">BSTR</span><span class="sxs-lookup"><span data-stu-id="eb1ec-162">BSTR</span></span>

<span data-ttu-id="eb1ec-p117">Um **BSTR** (**B**asic **STR**ing) é um tipo de dados estruturado que contém uma sequência de caracteres e seu comprimento. O COM fornece métodos para alocar, manipular e liberar **BSTR**.</span><span class="sxs-lookup"><span data-stu-id="eb1ec-p117">A **BSTR** (**B**asic **STR**ing) is a structured data type that contains a character string and the string's length. COM provides methods to allocate, manipulate, and free a **BSTR**.</span></span>

<span data-ttu-id="eb1ec-165">O \*\* \_bstr\_t\*\* classe encapsula e gerencia o tipo de dados **BSTR** .</span><span class="sxs-lookup"><span data-stu-id="eb1ec-165">The **\_bstr\_t** class encapsulates and manages the **BSTR** data type.</span></span>

<span data-ttu-id="eb1ec-166">Quando a referência de API do ADO informa que um método ou uma propriedade tem um valor **String** , isso significa que o valor é na forma de um \*\* \_bstr\_t\*\*.</span><span class="sxs-lookup"><span data-stu-id="eb1ec-166">When the ADO API Reference says a method or property takes a **String** value, it means the value is in the form of a **\_bstr\_t**.</span></span>

#### <a name="casting-variantt-and-bstrt-classes"></a><span data-ttu-id="eb1ec-167">Lançar \_variant\_t e \_bstr\_classes t</span><span class="sxs-lookup"><span data-stu-id="eb1ec-167">Casting \_variant\_t and \_bstr\_t classes</span></span>

<span data-ttu-id="eb1ec-168">Geralmente não é necessário ao código explicitamente um \*\* \_variant\_t\*\* ou \*\* \_bstr\_t\*\* em um argumento para uma operação.</span><span class="sxs-lookup"><span data-stu-id="eb1ec-168">Often it is not necessary to explicitly code a **\_variant\_t** or **\_bstr\_t** in an argument to an operation.</span></span> <span data-ttu-id="eb1ec-169">Se o \*\* \_variant\_t\*\* ou \*\* \_bstr\_t\*\* classe tem um construtor que corresponda ao tipo de dados do argumento, em seguida, o compilador irá gerar apropriada \*\* \_variant\_t\*\* ou \*\* \_ BSTR\_t\*\*.</span><span class="sxs-lookup"><span data-stu-id="eb1ec-169">If the **\_variant\_t** or **\_bstr\_t** class has a constructor that matches the data type of the argument, then the compiler will generate the appropriate **\_variant\_t** or **\_bstr\_t**.</span></span>

<span data-ttu-id="eb1ec-170">Entretanto, se o argumento for ambíguo, isto é, o tipo de dados do argumento for correspondente a mais de um construtor, será necessário orientar o argumento com o tipo de dados apropriado para chamar o construtor correto.</span><span class="sxs-lookup"><span data-stu-id="eb1ec-170">However, if the argument is ambiguous, that is, the argument's data type matches more than one constructor, you must cast the argument with the appropriate data type to invoke the correct constructor.</span></span>

<span data-ttu-id="eb1ec-171">Por exemplo, a declaração para o método **Recordset::Open** é:</span><span class="sxs-lookup"><span data-stu-id="eb1ec-171">For example, the declaration for the **Recordset::Open** method is:</span></span>

```vb 
 
 HRESULT Open ( 
 const _variant_t & Source, 
 const _variant_t & ActiveConnection, 
 enum CursorTypeEnum CursorType, 
 enum LockTypeEnum LockType, 
 long Options ); 
```

<span data-ttu-id="eb1ec-172">O argumento ActiveConnection utiliza uma referência para um \*\* \_variant\_t\*\*, que você pode código como uma cadeia de caracteres de conexão ou um ponteiro para um objeto de **Conexão** aberto.</span><span class="sxs-lookup"><span data-stu-id="eb1ec-172">The ActiveConnection argument takes a reference to a **\_variant\_t**, which you may code as a connection string or a pointer to an open **Connection** object.</span></span>

<span data-ttu-id="eb1ec-173">O correto \*\* \_variant\_t\*\* será construída implicitamente se você passar uma cadeia de caracteres, como "DSN = pubs; uid = sa; pwd =;", ou um ponteiro como "(IDispatch \*) pConn".</span><span class="sxs-lookup"><span data-stu-id="eb1ec-173">The correct **\_variant\_t** will be constructed implicitly if you pass a string such as "DSN=pubs;uid=sa;pwd=;", or a pointer such as "(IDispatch \*) pConn".</span></span>

<span data-ttu-id="eb1ec-174">Ou você pode codificar explicitamente um \*\* \_variant\_t\*\* contendo um ponteiro como "\_variant\_t ((IDispatch \*) pConn, true)".</span><span class="sxs-lookup"><span data-stu-id="eb1ec-174">Or you may explicitly code a **\_variant\_t** containing a pointer such as "\_variant\_t((IDispatch \*) pConn, true)".</span></span> <span data-ttu-id="eb1ec-175">A projeção, (IDispatch \*), resolva a ambiguidade com outro construtor que usa um ponteiro para uma interface IUnknown.</span><span class="sxs-lookup"><span data-stu-id="eb1ec-175">The cast, (IDispatch \*), resolves the ambiguity with another constructor that takes a pointer to an IUnknown interface.</span></span>

<span data-ttu-id="eb1ec-p120">Um ponto importante a ser mencionado é que o ADO é uma interface IDispatch. Sempre que um ponteiro para um objeto do ADO for transmitido como uma **Variant**, aquele ponteiro deve ser orientado como um ponteiro para uma interface IDispatch.</span><span class="sxs-lookup"><span data-stu-id="eb1ec-p120">It is a crucial, though seldom mentioned fact, that ADO is an IDispatch interface. Whenever a pointer to an ADO object must be passed as a **Variant**, that pointer must be cast as a pointer to an IDispatch interface.</span></span>

<span data-ttu-id="eb1ec-178">O último caso explicitamente codes o segundo argumento boolean do construtor com seu valor padrão opcional, true.</span><span class="sxs-lookup"><span data-stu-id="eb1ec-178">The last case explicitly codes the second boolean argument of the constructor with its optional, default value of true.</span></span> <span data-ttu-id="eb1ec-179">Este argumento faz com que o construtor de **Variant** chamar seu método de () **AddRef**, que indica de ADO automaticamente chamar o \*\* \_variant\_t::Release\*\*método () quando terminar a chamada de método ou uma propriedade do ADO.</span><span class="sxs-lookup"><span data-stu-id="eb1ec-179">This argument causes the **Variant** constructor to call its **AddRef**() method, which compensates for ADO automatically calling the **\_variant\_t::Release**() method when the ADO method or property call completes.</span></span>

### <a name="safearray"></a><span data-ttu-id="eb1ec-180">SafeArray</span><span class="sxs-lookup"><span data-stu-id="eb1ec-180">SafeArray</span></span>

<span data-ttu-id="eb1ec-181">**SafeArray** é um tipo de dados estruturado que contém uma matriz de outros tipos de dados.</span><span class="sxs-lookup"><span data-stu-id="eb1ec-181">A **SafeArray** is a structured data type that contains an array of other data types.</span></span> <span data-ttu-id="eb1ec-182">Um **SafeArray** é chamado *seguros* porque ele contém informações sobre os limites de cada dimensão de matriz e limita o acesso aos elementos de matriz dentro desses limites.</span><span class="sxs-lookup"><span data-stu-id="eb1ec-182">A **SafeArray** is called *safe* because it contains information about the bounds of each array dimension, and limits access to array elements within those bounds.</span></span>

<span data-ttu-id="eb1ec-183">Quando a Referência à API do ADO informa que um método ou uma propriedade tem ou retorna uma matriz, isso significa que o método ou a propriedade tem ou retorna **SafeArray**, não uma matriz C/C++ nativa.</span><span class="sxs-lookup"><span data-stu-id="eb1ec-183">When the ADO API Reference says a method or property takes or returns an array, it means the method or property takes or returns a **SafeArray**, not a native C/C++ array.</span></span>

<span data-ttu-id="eb1ec-p123">Por exemplo, o segundo parâmetro do método **OpenSchema** do objeto **Connection** requer uma matriz de valores **Variant**. Esses valores **Variant** devem ser transmitidos como elementos de **SafeArray**, e esse **SafeArray** deve ser definido como o valor de outra **Variant**. Isso significa que outra **Variant** é transmitida como o segundo argumento de **OpenSchema**.</span><span class="sxs-lookup"><span data-stu-id="eb1ec-p123">For example, the second parameter of the **Connection** object **OpenSchema** method requires an array of **Variant** values. Those **Variant** values must be passed as elements of a **SafeArray**, and that **SafeArray** must be set as the value of another **Variant**. It is that other **Variant** that is passed as the second argument of **OpenSchema**.</span></span>

<span data-ttu-id="eb1ec-187">Como exemplos adicionais, o primeiro argumento do método **Find** é uma **Variant** cujo valor é um **SafeArray** com uma dimensão; cada um dos argumentos principal e secundário opcionais de **AddNew** é um **SafeArray** com uma dimensão; e o valor de retorno do método **GetRows** é uma **Variant** cujo valor é um **SafeArray** com duas dimensões.</span><span class="sxs-lookup"><span data-stu-id="eb1ec-187">As further examples, the first argument of the **Find** method is a **Variant** whose value is a one-dimensional **SafeArray**; each of the optional first and second arguments of **AddNew** is a one-dimensional **SafeArray**; and the return value of the **GetRows** method is a **Variant** whose value is a two-dimensional **SafeArray**.</span></span>

## <a name="missing-and-default-parameters"></a><span data-ttu-id="eb1ec-188">Parâmetros ausentes e padrão</span><span class="sxs-lookup"><span data-stu-id="eb1ec-188">Missing and default parameters</span></span>

<span data-ttu-id="eb1ec-p124">O Visual Basic permite parâmetros Missing nos métodos. Por exemplo, o método **Open** do objeto **Recordset** tem cinco parâmetros, mas você pode ignorar os parâmetros intermediários e excluir os parâmetros à direita. Um **BSTR** ou **Variant** padrão será substituído dependendo do tipo de dados do operador ausente.</span><span class="sxs-lookup"><span data-stu-id="eb1ec-p124">Visual Basic allows missing parameters in methods. For example, the **Recordset** object **Open** method has five parameters, but you can skip intermediate parameters and leave off trailing parameters. A default **BSTR** or **Variant** will be substituted depending on the data type of the missing operand.</span></span>

<span data-ttu-id="eb1ec-192">Em C/C++, todos os operadores devem ser especificados.</span><span class="sxs-lookup"><span data-stu-id="eb1ec-192">In C/C++, all operands must be specified.</span></span> <span data-ttu-id="eb1ec-193">Se você deseja especificar um parâmetro missing cujo tipo de dados é uma cadeia de caracteres, especifique um \*\* \_bstr\_t\*\* que contém uma cadeia de caracteres nula.</span><span class="sxs-lookup"><span data-stu-id="eb1ec-193">If you want to specify a missing parameter whose data type is a string, specify a **\_bstr\_t** containing a null string.</span></span> <span data-ttu-id="eb1ec-194">Se você deseja especificar um parâmetro missing cujo tipo de dados é um **Variant**, especifique um \*\* \_variant\_t\*\* com um valor de DISP\_f\_PARAMNOTFOUND e um tipo de VT\_erro.</span><span class="sxs-lookup"><span data-stu-id="eb1ec-194">If you want to specify a missing parameter whose data type is a **Variant**, specify a **\_variant\_t** with a value of DISP\_E\_PARAMNOTFOUND and a type of VT\_ERROR.</span></span> <span data-ttu-id="eb1ec-195">Como alternativa, especifique o equivalente \*\* \_variant\_t\*\* constante, **vtMissing**, que é fornecido pelo \*\* \#importar\*\* diretiva.</span><span class="sxs-lookup"><span data-stu-id="eb1ec-195">Alternatively, specify the equivalent **\_variant\_t** constant, **vtMissing**, which is supplied by the **\#import** directive.</span></span>

<span data-ttu-id="eb1ec-p126">Três métodos são exceções ao uso típico de **vtMissing**. Eles são os métodos **Execute** dos objetos **Connection** e **Command**, e os métodos **NextRecordset** do objeto **Recordset**. A seguir estão suas assinaturas:</span><span class="sxs-lookup"><span data-stu-id="eb1ec-p126">Three methods are exceptions to the typical use of **vtMissing**. These are the **Execute** methods of the **Connection** and **Command** objects, and the **NextRecordset** method of the **Recordset** object. The following are their signatures:</span></span>

```vb 
 
_RecordsetPtr Invalid DDUE based on source, error:link not allowed in code, link filename:mdmthcnnexecute_HV10294345.xml( _bstr_t CommandText, VARIANT * RecordsAffected, 
 long Options ); // Connection 
_RecordsetPtr Invalid DDUE based on source, error:link not allowed in code, link filename:mdmthcmdexecute_HV10294344.xml( VARIANT * RecordsAffected, VARIANT * Parameters, 
 long Options ); // Command 
_RecordsetPtr Invalid DDUE based on source, error:link not allowed in code, link filename:mdmthnextrec_HV10294541.xml( VARIANT * RecordsAffected ); // Recordset 
```

<span data-ttu-id="eb1ec-p127">Os parâmetros *RecordsAffected* e *Parameters* são ponteiros para uma **Variant**. *Parameters* é um parâmetro de entrada que especifica o endereço de uma **Variant** contendo um único parâmetro, ou uma matriz de parâmetros, que modifica o comando que está sendo executado. *RecordsAffected* é um parâmetro de saída que especifica o endereço de uma **Variant**, em que o número de linhas afetadas pelo método é retornado.</span><span class="sxs-lookup"><span data-stu-id="eb1ec-p127">The parameters, *RecordsAffected* and *Parameters*, are pointers to a **Variant**. *Parameters* is an input parameter which specifies the address of a **Variant** containing a single parameter, or array of parameters, that will modify the command being executed. *RecordsAffected* is an output parameter that specifies the address of a **Variant**, where the number of rows affected by the method is returned.</span></span>

<span data-ttu-id="eb1ec-202">No objeto **Command** método **Execute** , indicar que nenhuma parâmetros forem especificados, definindo *parâmetros* para uma \&vtMissing (que é recomendado) ou para o ponteiro nulo (ou seja, **Nulo** ou zero (0)).</span><span class="sxs-lookup"><span data-stu-id="eb1ec-202">In the **Command** object **Execute** method, indicate that no parameters are specified by setting *Parameters* to either \&vtMissing (which is recommended) or to the null pointer (that is, **NULL** or zero (0)).</span></span> <span data-ttu-id="eb1ec-203">Se o *parâmetro* for definido como o ponteiro nulo, o método internamente substituirá o equivalente do **vtMissing**e conclui a operação.</span><span class="sxs-lookup"><span data-stu-id="eb1ec-203">If *Parameters* is set to the null pointer, the method internally substitutes the equivalent of **vtMissing**, and then completes the operation.</span></span>

<span data-ttu-id="eb1ec-204">Em todos os métodos, indica que o número de registros afetados não deve ser retornado, definindo *RecordsAffected* para o ponteiro nulo.</span><span class="sxs-lookup"><span data-stu-id="eb1ec-204">In all the methods, indicate that the number of records affected should not be returned by setting *RecordsAffected* to the null pointer.</span></span> <span data-ttu-id="eb1ec-205">Nesse caso, o ponteiro nulo não é mais um parâmetro Missing nem sequer uma indicação de que o método deve descartar o número de registros afetados.</span><span class="sxs-lookup"><span data-stu-id="eb1ec-205">In this case, the null pointer is not so much a missing parameter as an indication that the method should discard the number of records affected.</span></span>

<span data-ttu-id="eb1ec-206">Dessa forma, para esses três métodos, é válido codificar algo como:</span><span class="sxs-lookup"><span data-stu-id="eb1ec-206">Thus, for these three methods, it is valid to code something such as:</span></span>

```vb 
 
pConnection->Execute("commandText", NULL, adCmdText); 
pCommand->Execute(NULL, NULL, adCmdText); 
pRecordset->NextRecordset(NULL); 
```

## <a name="error-handling"></a><span data-ttu-id="eb1ec-207">Tratamento de erros</span><span class="sxs-lookup"><span data-stu-id="eb1ec-207">Error handling</span></span>

<span data-ttu-id="eb1ec-208">Em COM, a maioria das operações retorna um código HRESULT que indica se uma função foi concluída com êxito.</span><span class="sxs-lookup"><span data-stu-id="eb1ec-208">In COM, most operations return an HRESULT return code that indicates whether a function completed successfully.</span></span> <span data-ttu-id="eb1ec-209">O \*\* \#importar\*\* diretiva gera um código de wrapper ao redor de cada propriedade ou método "raw" e verifica o HRESULT retornado.</span><span class="sxs-lookup"><span data-stu-id="eb1ec-209">The **\#import** directive generates wrapper code around each "raw" method or property and checks the returned HRESULT.</span></span> <span data-ttu-id="eb1ec-210">Se o HRESULT indica uma falha, o código de wrapper lança um erro COM chamando \_com\_problema\_errorex() com o HRESULT retornar código como um argumento.</span><span class="sxs-lookup"><span data-stu-id="eb1ec-210">If the HRESULT indicates failure, the wrapper code throws a COM error by calling \_com\_issue\_errorex() with the HRESULT return code as an argument.</span></span> <span data-ttu-id="eb1ec-211">Os objetos de erro do COM podem ser capturados em um bloco **try**-**catch**.</span><span class="sxs-lookup"><span data-stu-id="eb1ec-211">COM error objects can be caught in a **try**-**catch** block.</span></span> <span data-ttu-id="eb1ec-212">(Para a mesma da eficiência, catch uma referência a um \*\* \_com\_erro\*\* objeto.)</span><span class="sxs-lookup"><span data-stu-id="eb1ec-212">(For efficiency's sake, catch a reference to a **\_com\_error** object.)</span></span>

<span data-ttu-id="eb1ec-p131">Lembre-se, esses são os erros do ADO: eles resultam de falha em operações do ADO. Os erros retornados pelo provedor subjacente aparecem como objetos **Error** na coleção **Errors** do objeto **Connection**.</span><span class="sxs-lookup"><span data-stu-id="eb1ec-p131">Remember, these are ADO errors: they result from the ADO operation failing. Errors returned by the underlying provider appear as **Error** objects in the **Connection** object **Errors** collection.</span></span>

<span data-ttu-id="eb1ec-215">O \*\* \#importar\*\* diretiva cria apenas erro rotinas de tratamento de métodos e propriedades declaradas na ADO. dll.</span><span class="sxs-lookup"><span data-stu-id="eb1ec-215">The **\#import** directive creates only error handling routines for methods and properties declared in the ADO .dll.</span></span> <span data-ttu-id="eb1ec-216">Contudo, você pode aproveitar esse mesmo mecanismo de tratamento de erros escrevendo sua própria macro de verificação de erros ou sua função inline.</span><span class="sxs-lookup"><span data-stu-id="eb1ec-216">However, you can take advantage of this same error handling mechanism by writing your own error checking macro or inline function.</span></span> <span data-ttu-id="eb1ec-217">Consulte o tópico [Extensões do Visual C++](visual-c-extensions-for-ado.md) ou o código nas seções a seguir para obter exemplos.</span><span class="sxs-lookup"><span data-stu-id="eb1ec-217">See the topic, [Visual C++ Extensions](visual-c-extensions-for-ado.md), or the code in the following sections for examples.</span></span>

## <a name="visual-c-equivalents-of-visual-basic-conventions"></a><span data-ttu-id="eb1ec-218">Equivalentes de Visual C++ de convenções do Visual Basic</span><span class="sxs-lookup"><span data-stu-id="eb1ec-218">Visual C++ equivalents of Visual Basic conventions</span></span>

<span data-ttu-id="eb1ec-219">A seguir está um resumo de várias convenções na documentação do ADO, codificadas no Visual Basic, bem como seus equivalentes no Visual C++.</span><span class="sxs-lookup"><span data-stu-id="eb1ec-219">The following is a summary of several conventions in the ADO documentation, coded in Visual Basic, as well as their equivalents in Visual C++.</span></span>

### <a name="declaring-an-ado-object"></a><span data-ttu-id="eb1ec-220">Declarando um objeto ADO</span><span class="sxs-lookup"><span data-stu-id="eb1ec-220">Declaring an ADO object</span></span>

<span data-ttu-id="eb1ec-221">No Visual Basic, uma variável de objeto do ADO (nesse caso para um objeto **Recordset** ) é declarada como se segue:</span><span class="sxs-lookup"><span data-stu-id="eb1ec-221">In Visual Basic, an ADO object variable (in this case for a **Recordset** object) is declared as follows:</span></span>

```vb 
 
Dim rst As ADODB.Recordset 
```

<span data-ttu-id="eb1ec-222">A cláusula, "ADODB. Recordset", é o ProgID do objeto **Recordset** , conforme definido no registro.</span><span class="sxs-lookup"><span data-stu-id="eb1ec-222">The clause, "ADODB.Recordset", is the ProgID of the **Recordset** object as defined in the Registry.</span></span> <span data-ttu-id="eb1ec-223">Uma nova instância de um objeto **Record** é declarado como a seguir:</span><span class="sxs-lookup"><span data-stu-id="eb1ec-223">A new instance of a **Record** object is declared as follows:</span></span>

```vb 
 
Dim rst As New ADODB.Recordset 
```

<span data-ttu-id="eb1ec-224">\-ou -</span><span class="sxs-lookup"><span data-stu-id="eb1ec-224">\-or-</span></span>

```vb 
 
Dim rst As ADODB.Recordset 
Set rst = New ADODB.Recordset 
```

<span data-ttu-id="eb1ec-225">No Visual C++, o \*\* \#importar\*\* diretiva gera declarações de tipo de ponteiro inteligente para todos os objetos do ADO.</span><span class="sxs-lookup"><span data-stu-id="eb1ec-225">In Visual C++, the **\#import** directive generates smart pointer-type declarations for all the ADO objects.</span></span> <span data-ttu-id="eb1ec-226">Por exemplo, uma variável que aponta para um \*\* \_Recordset\*\* objeto é do tipo \*\* \_RecordsetPtr\*\*e é declarada como se segue:</span><span class="sxs-lookup"><span data-stu-id="eb1ec-226">For example, a variable that points to a **\_Recordset** object is of type **\_RecordsetPtr**, and is declared as follows:</span></span>

```cpp 
 
_RecordsetPtr rs; 
```

<span data-ttu-id="eb1ec-227">Uma variável que aponta para uma nova instância de um \*\* \_Recordset\*\* objeto é declarado como se segue:</span><span class="sxs-lookup"><span data-stu-id="eb1ec-227">A variable that points to a new instance of a **\_Recordset** object is declared as follows:</span></span>

```cpp 
 
_RecordsetPtr rs("ADODB.Recordset"); 
```

<span data-ttu-id="eb1ec-228">\-ou -</span><span class="sxs-lookup"><span data-stu-id="eb1ec-228">\-or-</span></span>

```cpp 
 
_RecordsetPtr rs; 
rs.CreateInstance("ADODB.Recordset"); 
```

<span data-ttu-id="eb1ec-229">\-ou -</span><span class="sxs-lookup"><span data-stu-id="eb1ec-229">\-or-</span></span>

```cpp 
 
_RecordsetPtr rs; 
rs.CreateInstance(__uuidof(_Recordset)); 
```

<span data-ttu-id="eb1ec-230">Depois que o método **CreateInstance** é chamado, a variável pode ser utilizada como se segue:</span><span class="sxs-lookup"><span data-stu-id="eb1ec-230">After the **CreateInstance** method is called, the variable can be used as follows:</span></span>

```cpp 
 
rs->Open(...); 
```

<span data-ttu-id="eb1ec-231">Observe que, em um caso, o "." operador é usado como se a variável fosse uma instância de uma classe (rs. CreateInstance) e em outro caso, o "-\>" operador é usado como se a variável fosse um ponteiro para uma interface (rs -\>Open).</span><span class="sxs-lookup"><span data-stu-id="eb1ec-231">Notice that in one case, the "." operator is used as if the variable were an instance of a class (rs.CreateInstance), and in another case, the "-\>" operator is used as if the variable were a pointer to an interface (rs-\>Open).</span></span>

<span data-ttu-id="eb1ec-232">Uma variável pode ser usada de duas maneiras, porque o "-\>" operador está sobrecarregado para permitir que uma instância de uma classe para que atue como um ponteiro para uma interface.</span><span class="sxs-lookup"><span data-stu-id="eb1ec-232">One variable can be used in two ways because the "-\>" operator is overloaded to allow an instance of a class to behave like a pointer to an interface.</span></span> <span data-ttu-id="eb1ec-233">Um membro da classe privada da variável instância contém um ponteiro para o \*\* \_Recordset\*\* interface; o "-\>" operador retorna desse ponteiro; e o ponteiro retornado acessa os membros a \*\* \_Recordset\*\* objeto.</span><span class="sxs-lookup"><span data-stu-id="eb1ec-233">A private class member of the instance variable contains a pointer to the **\_Recordset** interface; the "-\>" operator returns that pointer; and the returned pointer accesses the members of the **\_Recordset** object.</span></span>

### <a name="coding-a-missing-parameter"></a><span data-ttu-id="eb1ec-234">Codificando um parâmetro missing</span><span class="sxs-lookup"><span data-stu-id="eb1ec-234">Coding a missing parameter</span></span>

#### <a name="string"></a><span data-ttu-id="eb1ec-235">Cadeia de caracteres</span><span class="sxs-lookup"><span data-stu-id="eb1ec-235">String</span></span>

<span data-ttu-id="eb1ec-236">Quando é necessário codificar um operador **String** ausente no Visual Basic, você simplesmente omite o operador.</span><span class="sxs-lookup"><span data-stu-id="eb1ec-236">When you need to code a missing **String** operand in Visual Basic, you merely omit the operand.</span></span> <span data-ttu-id="eb1ec-237">Você deve especificar o operador no Visual C++.</span><span class="sxs-lookup"><span data-stu-id="eb1ec-237">You must specify the operand in Visual C++.</span></span> <span data-ttu-id="eb1ec-238">Código um \*\* \_bstr\_t\*\* que tem uma sequência vazia como um valor.</span><span class="sxs-lookup"><span data-stu-id="eb1ec-238">Code a **\_bstr\_t** that has an empty string as a value.</span></span>

```cpp 
 
_bstr_t strMissing(L""); 
```

#### <a name="variant"></a><span data-ttu-id="eb1ec-239">Variant</span><span class="sxs-lookup"><span data-stu-id="eb1ec-239">Variant</span></span>

<span data-ttu-id="eb1ec-240">Quando é necessário codificar um operador **Variant** ausente no Visual Basic, você simplesmente omite o operador.</span><span class="sxs-lookup"><span data-stu-id="eb1ec-240">When you need to code a missing **Variant** operand in Visual Basic, you merely omit the operand.</span></span> <span data-ttu-id="eb1ec-241">Você deve especificar todos os operadores no Visual C++.</span><span class="sxs-lookup"><span data-stu-id="eb1ec-241">You must specify all operands in Visual C++.</span></span> <span data-ttu-id="eb1ec-242">Código um parâmetro **Variant** missing com um \*\* \_variant\_t\*\* definido como o valor especial, DISP\_f\_PARAMNOTFOUND e tipo, VT\_erro.</span><span class="sxs-lookup"><span data-stu-id="eb1ec-242">Code a missing **Variant** parameter with a **\_variant\_t** set to the special value, DISP\_E\_PARAMNOTFOUND, and type, VT\_ERROR.</span></span> <span data-ttu-id="eb1ec-243">Como alternativa, especificar **vtMissing**, que é equivalente a uma constante pré-definidos fornecidos pelo \*\* \#importar\*\* diretiva.</span><span class="sxs-lookup"><span data-stu-id="eb1ec-243">Alternatively, specify **vtMissing**, which is an equivalent pre-defined constant supplied by the **\#import** directive.</span></span>

```cpp 
 
_variant_t vtMissingYours(DISP_E_PARAMNOTFOUND, VT_ERROR); 
```

<span data-ttu-id="eb1ec-244">\-ou uso-</span><span class="sxs-lookup"><span data-stu-id="eb1ec-244">\-or use -</span></span>

```cpp 
 
...vtMissing...; 
```

### <a name="declaring-a-variant"></a><span data-ttu-id="eb1ec-245">Declarando uma variant</span><span class="sxs-lookup"><span data-stu-id="eb1ec-245">Declaring a variant</span></span>

<span data-ttu-id="eb1ec-246">No Visual Basic, uma **Variant** é declarada como a instrução **Dim** como se segue:</span><span class="sxs-lookup"><span data-stu-id="eb1ec-246">In Visual Basic, a **Variant** is declared with the **Dim** statement as follows:</span></span>

```vb 
 
Dim VariableName As Variant 
```

<span data-ttu-id="eb1ec-247">No Visual C++, declare uma variável como tipo \*\* \_variant\_t\*\*.</span><span class="sxs-lookup"><span data-stu-id="eb1ec-247">In Visual C++, declare a variable as type **\_variant\_t**.</span></span> <span data-ttu-id="eb1ec-248">Alguns esquemático \*\* \_variant\_t\*\* declarações são mostradas abaixo.</span><span class="sxs-lookup"><span data-stu-id="eb1ec-248">A few schematic **\_variant\_t** declarations are shown below.</span></span>

> [!NOTE]
> <span data-ttu-id="eb1ec-p139">[!OBSERVAçãO] Essas declarações fornecem uma pequena ideia do que você codificaria em seu próprio programa. Para obter mais informações, consulte os exemplos abaixo e a documentação do Visual C++.</span><span class="sxs-lookup"><span data-stu-id="eb1ec-p139">These declarations merely give a rough idea of what you would code in your own program. For more information, see the examples below, and the Visual C++ documentation.</span></span>

```cpp 
 
_variant_t VariableName(value); 
_variant_t VariableName((data type cast) value); 
_variant_t VariableName(value, VT_DATATYPE); 
_variant_t VariableName(interface * value, bool fAddRef = true); 
```

### <a name="using-arrays-of-variants"></a><span data-ttu-id="eb1ec-251">Utilizando matrizes de variants</span><span class="sxs-lookup"><span data-stu-id="eb1ec-251">Using arrays of variants</span></span>

<span data-ttu-id="eb1ec-252">No Visual Basic, as matrizes de **Variants** podem ser codificadas com a instrução **Dim** ou podem utilizar a função **Array**, como demonstrado no seguinte código de exemplo:</span><span class="sxs-lookup"><span data-stu-id="eb1ec-252">In Visual Basic, arrays of **Variants** can be coded with the **Dim** statement, or you may use the **Array** function, as demonstrated in the following example code:</span></span>

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

<span data-ttu-id="eb1ec-253">O exemplo a seguir do Visual C++ demonstra o uso de **SafeArray** utilizado com um \*\* \_variant\_t\*\*.</span><span class="sxs-lookup"><span data-stu-id="eb1ec-253">The following Visual C++ example demonstrates using a **SafeArray** used with a **\_variant\_t**.</span></span>

> [!NOTE]
> <span data-ttu-id="eb1ec-254">[!OBSERVAçãO] As seguintes notas correspondem às seções comentadas no exemplo de código.</span><span class="sxs-lookup"><span data-stu-id="eb1ec-254">The following notes correspond to commented sections in the code example.</span></span>

1. <span data-ttu-id="eb1ec-255">Novamente, a função inline TESTHR() é definida para aproveitar a existência do mecanismo de tratamento de erros.</span><span class="sxs-lookup"><span data-stu-id="eb1ec-255">Once again, the TESTHR() inline function is defined to take advantage of the existing error-handling mechanism.</span></span>

2. <span data-ttu-id="eb1ec-p140">Você precisa apenas de uma matriz com uma dimensão para poder utilizar **SafeArrayCreateVector**, em vez da declaração **SAFEARRAYBOUND** e da função **SafeArrayCreate** de objetivos gerais. A seguir está um exemplo de como o código é, usando **SafeArrayCreate**:</span><span class="sxs-lookup"><span data-stu-id="eb1ec-p140">You only need a one-dimensional array, so you can use **SafeArrayCreateVector**, instead of the general purpose **SAFEARRAYBOUND** declaration and **SafeArrayCreate** function. The following is what that code would look like using **SafeArrayCreate**:</span></span>
    
   ```cpp 
     
     SAFEARRAYBOUND sabound[1]; 
     sabound[0].lLbound = 0; 
     sabound[0].cElements = 4; 
     pSa = SafeArrayCreate(VT_VARIANT, 1, sabound); 
   ```

3. <span data-ttu-id="eb1ec-258">O esquema identificado pela constante enumerada, **adSchemaColumns**, é associado a quatro colunas de restrição: tabela\_catálogo, tabela\_esquema, tabela\_nome e a coluna\_nome.</span><span class="sxs-lookup"><span data-stu-id="eb1ec-258">The schema identified by the enumerated constant, **adSchemaColumns**, is associated with four constraint columns: TABLE\_CATALOG, TABLE\_SCHEMA, TABLE\_NAME, and COLUMN\_NAME.</span></span> <span data-ttu-id="eb1ec-259">Portanto, uma matriz de valores **Variant** com quatro elementos é criada.</span><span class="sxs-lookup"><span data-stu-id="eb1ec-259">Therefore, an array of **Variant** values with four elements is created.</span></span> <span data-ttu-id="eb1ec-260">Em seguida, um valor de restrição que corresponde à tabela, a terceira coluna\_nome, for especificado.</span><span class="sxs-lookup"><span data-stu-id="eb1ec-260">Then a constraint value that corresponds to the third column, TABLE\_NAME, is specified.</span></span> <span data-ttu-id="eb1ec-261">O **Recordset** retornado consiste em várias colunas, um subconjunto de colunas de restrição.</span><span class="sxs-lookup"><span data-stu-id="eb1ec-261">The **Recordset** that is returned consists of several columns, a subset of which is the constraint columns.</span></span> <span data-ttu-id="eb1ec-262">Os valores das colunas de restrição para cada linha retornada deve ser igual aos valores de restrição correspondentes.</span><span class="sxs-lookup"><span data-stu-id="eb1ec-262">The values of the constraint columns for each returned row must be the same as the corresponding constraint values.</span></span>

4. <span data-ttu-id="eb1ec-263">Aqueles que estão familiarizados com **SafeArrays** podem-se que **SafeArrayDestroy**(de) não é chamado antes de sair.</span><span class="sxs-lookup"><span data-stu-id="eb1ec-263">Those familiar with **SafeArrays** may be surprised that **SafeArrayDestroy**() is not called before the exit.</span></span> <span data-ttu-id="eb1ec-264">Na verdade, chamar () de **SafeArrayDestroy**neste caso fará com que uma exceção de tempo de execução.</span><span class="sxs-lookup"><span data-stu-id="eb1ec-264">In fact, calling **SafeArrayDestroy**() in this case will cause a run-time exception.</span></span> <span data-ttu-id="eb1ec-265">O motivo é que o destrutor para vtCriteria chamará () de **VariantClear**quando o \*\* \_variant\_t\*\* sai do escopo, qual liberará **SafeArray**.</span><span class="sxs-lookup"><span data-stu-id="eb1ec-265">The reason is that the destructor for vtCriteria will call **VariantClear**() when the **\_variant\_t** goes out of scope, which will free the **SafeArray**.</span></span> <span data-ttu-id="eb1ec-266">Chamar **SafeArrayDestroy**, sem limpando manualmente o \*\* \_variant\_t\*\*, causaria o destrutor tentar limpar um ponteiro **SafeArray** inválido.</span><span class="sxs-lookup"><span data-stu-id="eb1ec-266">Calling **SafeArrayDestroy**, without manually clearing the **\_variant\_t**, would cause the destructor to try to clear an invalid **SafeArray** pointer.</span></span> <span data-ttu-id="eb1ec-267">Se **SafeArrayDestroy** for chamado, o código será parecido com:</span><span class="sxs-lookup"><span data-stu-id="eb1ec-267">If **SafeArrayDestroy** were called, the code would look like this:</span></span>
    
   ```cpp 
     
     TESTHR(SafeArrayDestroy(pSa)); 
     vtCriteria.vt = VT_EMPTY; 
     vtCriteria.parray = NULL; 
   ```
    
   <span data-ttu-id="eb1ec-268">No entanto, é muito mais simples permitir que o \*\* \_variant\_t\*\* gerencie **SafeArray**.</span><span class="sxs-lookup"><span data-stu-id="eb1ec-268">However, it is much simpler to let the **\_variant\_t** manage the **SafeArray**.</span></span>


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

### <a name="using-property-getputputref"></a><span data-ttu-id="eb1ec-269">Use a propriedade Get/Put/PutRef</span><span class="sxs-lookup"><span data-stu-id="eb1ec-269">Using property Get/Put/PutRef</span></span>

<span data-ttu-id="eb1ec-270">No Visual Basic, o nome de uma propriedade não é qualificado se ela for recuperada, atribuída ou atribuída a uma referência.</span><span class="sxs-lookup"><span data-stu-id="eb1ec-270">In Visual Basic, the name of a property is not qualified by whether it is retrieved, assigned, or assigned a reference.</span></span>

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

<span data-ttu-id="eb1ec-271">Este exemplo do Visual C++ demonstra **Get**/**colocar**/\**PutRef \* \* \* propriedade*.</span><span class="sxs-lookup"><span data-stu-id="eb1ec-271">This Visual C++ example demonstrates the **Get**/**Put**/\**PutRef\*\*\*Property*.</span></span>

> [!NOTE]
> <span data-ttu-id="eb1ec-272">[!OBSERVAçãO] As seguintes notas correspondem às seções comentadas no exemplo de código.</span><span class="sxs-lookup"><span data-stu-id="eb1ec-272">The following notes correspond to commented sections in the code example.</span></span>

1. <span data-ttu-id="eb1ec-273">Este exemplo usa duas formas de um argumento de cadeia de caracteres ausente: uma constante explícita, **strMissing**e uma cadeia de caracteres que o compilador irá usar para criar um temporário \*\* \_bstr\_t\*\* que continuará a existir para o escopo do método **Open** .</span><span class="sxs-lookup"><span data-stu-id="eb1ec-273">This example uses two forms of a missing string argument: an explicit constant, **strMissing**, and a string that the compiler will use to create a temporary **\_bstr\_t** that will exist for the scope of the **Open** method.</span></span>

2. <span data-ttu-id="eb1ec-274">Não é necessário orientar o operador de rs -\>Putrefactiveconnection para (IDispatch \*) porque o tipo do operador já é (IDispatch \*).</span><span class="sxs-lookup"><span data-stu-id="eb1ec-274">It isn't necessary to cast the operand of rs-\>PutRefActiveConnection(cn) to (IDispatch \*) because the type of the operand is already (IDispatch \*).</span></span>
    
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

### <a name="using-getitemx-and-itemx"></a><span data-ttu-id="eb1ec-275">Utilizando GetItem e Item\[x\]</span><span class="sxs-lookup"><span data-stu-id="eb1ec-275">Using GetItem(x) and Item\[x\]</span></span>

<span data-ttu-id="eb1ec-276">Esse exemplo do Visual Basic demonstra a sintaxe padrão e alternativa para **Item**().</span><span class="sxs-lookup"><span data-stu-id="eb1ec-276">This Visual Basic example demonstrates the standard and alternative syntax for **Item**().</span></span>

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

<span data-ttu-id="eb1ec-277">Esse exemplo do Visual C++ demonstra **Item**.</span><span class="sxs-lookup"><span data-stu-id="eb1ec-277">This Visual C++ example demonstrates **Item**.</span></span>

> [!NOTE]
> <span data-ttu-id="eb1ec-278">[!OBSERVAçãO] A seguinte nota corresponde às seções comentadas no exemplo de código.</span><span class="sxs-lookup"><span data-stu-id="eb1ec-278">The following note corresponds to commented sections in the code example.</span></span>

1. <span data-ttu-id="eb1ec-279">Quando a coleção é acessada com **Item**, o índice **2** deve ser orientado para **long** para que um construtor apropriado seja chamado.</span><span class="sxs-lookup"><span data-stu-id="eb1ec-279">When the collection is accessed with **Item**, the index, **2**, must be cast to **long** so an appropriate constructor will be invoked.</span></span>
    
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

### <a name="casting-ado-object-pointers-with-idispatch-"></a><span data-ttu-id="eb1ec-280">Orientando ponteiros de objeto do ADO com (IDispatch \*)</span><span class="sxs-lookup"><span data-stu-id="eb1ec-280">Casting ADO object pointers with (IDispatch \*)</span></span>

<span data-ttu-id="eb1ec-281">O seguinte exemplo do Visual C++ demonstra o uso de (IDispatch \*) para orientar ponteiros de objetos do ADO.</span><span class="sxs-lookup"><span data-stu-id="eb1ec-281">The following Visual C++ example demonstrates using (IDispatch \*) to cast ADO object pointers.</span></span>

> [!NOTE]
> <span data-ttu-id="eb1ec-282">[!OBSERVAçãO] As seguintes notas correspondem às seções comentadas no exemplo de código.</span><span class="sxs-lookup"><span data-stu-id="eb1ec-282">The following notes correspond to commented sections in the code example.</span></span>

1. <span data-ttu-id="eb1ec-283">Especifique um objeto **Connection** de abertura em uma **Variant** explicitamente codificada.</span><span class="sxs-lookup"><span data-stu-id="eb1ec-283">Specify an open **Connection** object in an explicitly coded **Variant**.</span></span> <span data-ttu-id="eb1ec-284">Convertê-lo com (IDispatch \*) para o construtor correto seja chamado.</span><span class="sxs-lookup"><span data-stu-id="eb1ec-284">Cast it with (IDispatch \*) so the correct constructor will be invoked.</span></span> <span data-ttu-id="eb1ec-285">Além disso, definir explicitamente a segunda \*\* \_variant\_t\*\* parâmetro para o valor padrão **true**, portanto a contagem de referência do objeto será correta quando a operação de **Recordset** for encerrada.</span><span class="sxs-lookup"><span data-stu-id="eb1ec-285">Also, explicitly set the second **\_variant\_t** parameter to the default value of **true**, so the object reference count will be correct when the **Recordset::Open** operation ends.</span></span>

2. <span data-ttu-id="eb1ec-286">A expressão, (\_bstr\_t), não é uma projeção, mas um \*\* \_variant\_t\*\* operador que extrai um \*\* \_bstr\_t\*\* cadeia de caracteres de **Variant** retornado por **valor**.</span><span class="sxs-lookup"><span data-stu-id="eb1ec-286">The expression, (\_bstr\_t), is not a cast, but a **\_variant\_t** operator that extracts a **\_bstr\_t** string from the **Variant** returned by **Value**.</span></span> <span data-ttu-id="eb1ec-287">A expressão, (char\*), não é uma projeção, mas um \*\* \_bstr\_t\*\* operador que extrai um ponteiro para a cadeia de caracteres encapsulado em um \*\* \_bstr\_t\*\* objeto.</span><span class="sxs-lookup"><span data-stu-id="eb1ec-287">The expression, (char\*), is not a cast, but a **\_bstr\_t** operator that extracts a pointer to the encapsulated string in a **\_bstr\_t** object.</span></span> <span data-ttu-id="eb1ec-288">Esta seção do código demonstra algumas dos comportamentos útil da \*\* \_variant\_t\*\* e \*\* \_bstr\_t\*\* operadores.</span><span class="sxs-lookup"><span data-stu-id="eb1ec-288">This section of code demonstrates some of the useful behaviors of **\_variant\_t** and **\_bstr\_t** operators.</span></span>
    
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

