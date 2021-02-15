---
title: Glossário do ActiveX Data Objects (ADO)
TOCTitle: ADO Glossary
ms:assetid: 40f00876-7525-4117-8f57-f3d87c54be99
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249184(v=office.15)
ms:contentKeyID: 48544438
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 7ecb6208a8c970f037cb0ac699c947544eb8f547
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32284831"
---
# <a name="ado-glossary"></a><span data-ttu-id="6fc9f-102">Glossário do ADO</span><span class="sxs-lookup"><span data-stu-id="6fc9f-102">ADO glossary</span></span>

<span data-ttu-id="6fc9f-103">**Aplica-se ao:** Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="6fc9f-103">**Applies to**: Access 2013, Office 2013</span></span>

## <a name="a"></a><span data-ttu-id="6fc9f-104">A</span><span class="sxs-lookup"><span data-stu-id="6fc9f-104">A</span></span>

<span data-ttu-id="6fc9f-105">**URL absoluta**</span><span class="sxs-lookup"><span data-stu-id="6fc9f-105">**absolute URL**</span></span>

<span data-ttu-id="6fc9f-106">Uma URL totalmente qualificada que especifica o local de um recurso que reside na Internet ou em uma intranet.</span><span class="sxs-lookup"><span data-stu-id="6fc9f-106">A fully qualified URL that specifies the location of a resource that resides on the Internet or an intranet.</span></span> <span data-ttu-id="6fc9f-107">Consulte também **URL** e **URL relativa.**</span><span class="sxs-lookup"><span data-stu-id="6fc9f-107">See also **URL** and **relative URL**.</span></span>

<span data-ttu-id="6fc9f-108">**Controle ActiveX**</span><span class="sxs-lookup"><span data-stu-id="6fc9f-108">**ActiveX control**</span></span>

<span data-ttu-id="6fc9f-109">Auto-registro de componente COM dentro do processo que geralmente tem um elemento visual no tempo de design ou em tempo de executar.</span><span class="sxs-lookup"><span data-stu-id="6fc9f-109">Self-registering, in-process COM component that often has a visual element either at design time or run time.</span></span> <span data-ttu-id="6fc9f-110">Os controles ActiveX também têm a capacidade de se comunicar com um contêiner do Documento Ativo, como o Microsoft Internet Explorer.</span><span class="sxs-lookup"><span data-stu-id="6fc9f-110">ActiveX controls also have the ability to communicate with an Active Document container, such as Microsoft Internet Explorer.</span></span>

<span data-ttu-id="6fc9f-111">**ADISAPI (Advanced Data Internet Server Application Programming Interface)**</span><span class="sxs-lookup"><span data-stu-id="6fc9f-111">**ADISAPI (Advanced Data Internet Server Application Programming Interface)**</span></span>

<span data-ttu-id="6fc9f-112">Uma DLL ISAPI que fornece análise, controle de automação, empacotamento de **Recordset** e empacotamento MIME.</span><span class="sxs-lookup"><span data-stu-id="6fc9f-112">An ISAPI DLL that provides parsing, Automation control, **Recordset** marshaling, and MIME packaging.</span></span> <span data-ttu-id="6fc9f-113">O componente ADISAPI funciona por meio da API fornecida pelos Serviços de Informações da Internet (IIS).</span><span class="sxs-lookup"><span data-stu-id="6fc9f-113">The ADISAPI component works through the API provided by Internet Information Services (IIS).</span></span> <span data-ttu-id="6fc9f-114">Consulte também **ISAPI**.</span><span class="sxs-lookup"><span data-stu-id="6fc9f-114">See also **ISAPI**.</span></span>

<span data-ttu-id="6fc9f-115">**função de agregação**</span><span class="sxs-lookup"><span data-stu-id="6fc9f-115">**aggregate function**</span></span>

<span data-ttu-id="6fc9f-116">Em uma consulta, uma função como COUNT, AVG ou STDEV que calcula um valor usando todas as linhas em uma coluna de uma tabela.</span><span class="sxs-lookup"><span data-stu-id="6fc9f-116">In a query, a function such as COUNT, AVG, or STDEV that calculates a value using all the rows in a column of a table.</span></span> <span data-ttu-id="6fc9f-117">Ao escrever expressões e programar, você pode usar funções agregadas do SQL (incluindo as três listadas acima) e funções agregadas de domínio para determinar várias estatísticas.</span><span class="sxs-lookup"><span data-stu-id="6fc9f-117">In writing expressions and in programming, you can use SQL aggregate functions (including the three listed above) and domain aggregate functions to determine various statistics.</span></span>

<span data-ttu-id="6fc9f-118">**alias**</span><span class="sxs-lookup"><span data-stu-id="6fc9f-118">**alias**</span></span>

<span data-ttu-id="6fc9f-119">Um nome alternativo que você dá a uma coluna ou expressão em uma instrução SQL SELECT, geralmente mais curto ou mais significativo.</span><span class="sxs-lookup"><span data-stu-id="6fc9f-119">An alternate name you give to a column or expression in an SQL SELECT statement, often shorter or more meaningful.</span></span> <span data-ttu-id="6fc9f-120">Por exemplo, BobSales é o alias na seguinte instrução SELECT: "Select wr-Sales as BobSales from SalesDB".</span><span class="sxs-lookup"><span data-stu-id="6fc9f-120">For example, BobSales is the alias in the following SELECT statement: "Select wr-Sales as BobSales from SalesDB".</span></span> <span data-ttu-id="6fc9f-121">Um alias pode ser usado para atribuir dinamicamente colunas para controlar associações no **objeto DataControl** .</span><span class="sxs-lookup"><span data-stu-id="6fc9f-121">An alias can be used to dynamically assign columns to control bindings on the **DataControl** object.</span></span>

<span data-ttu-id="6fc9f-122">**threading de apartment**</span><span class="sxs-lookup"><span data-stu-id="6fc9f-122">**apartment threading**</span></span>

<span data-ttu-id="6fc9f-123">Um modelo de threading COM em que todas as chamadas para um objeto ocorrem em um thread.</span><span class="sxs-lookup"><span data-stu-id="6fc9f-123">A COM threading model where all calls to an object occur on one thread.</span></span> <span data-ttu-id="6fc9f-124">No threading de apartment, COM sincroniza e empacota chamadas.</span><span class="sxs-lookup"><span data-stu-id="6fc9f-124">In apartment threading, COM synchronizes and marshals calls.</span></span> <span data-ttu-id="6fc9f-125">Consulte também **COM**.</span><span class="sxs-lookup"><span data-stu-id="6fc9f-125">See also **COM**.</span></span>

<span data-ttu-id="6fc9f-126">**operação assíncrona**</span><span class="sxs-lookup"><span data-stu-id="6fc9f-126">**asynchronous operation**</span></span>

<span data-ttu-id="6fc9f-127">Uma operação que retorna o controle para o programa de chamada sem aguardar a conclusão da operação.</span><span class="sxs-lookup"><span data-stu-id="6fc9f-127">An operation that returns control to the calling program without waiting for the operation to complete.</span></span> <span data-ttu-id="6fc9f-128">Antes que a operação seja concluída, a execução do código continua.</span><span class="sxs-lookup"><span data-stu-id="6fc9f-128">Before the operation is complete, code execution continues.</span></span> <span data-ttu-id="6fc9f-129">Consulte também **a operação síncrona.**</span><span class="sxs-lookup"><span data-stu-id="6fc9f-129">See also **synchronous operation**.</span></span>

<span data-ttu-id="6fc9f-130">Retornar ao início</span><span class="sxs-lookup"><span data-stu-id="6fc9f-130">Return to top</span></span>

## <a name="b"></a><span data-ttu-id="6fc9f-131">B</span><span class="sxs-lookup"><span data-stu-id="6fc9f-131">B</span></span>

<span data-ttu-id="6fc9f-132">**entrada de associação**</span><span class="sxs-lookup"><span data-stu-id="6fc9f-132">**binding entry**</span></span>

<span data-ttu-id="6fc9f-133">Um mapeamento entre um campo em uma tabela e uma variável.</span><span class="sxs-lookup"><span data-stu-id="6fc9f-133">A mapping between a field in a table and a variable.</span></span> <span data-ttu-id="6fc9f-134">Nas extensões do ADO Visual C++, os **campos do Recordset** são mapeados para variáveis C/C++.</span><span class="sxs-lookup"><span data-stu-id="6fc9f-134">In the ADO Visual C++ extensions, **Recordset** fields are mapped to C/C++ variables.</span></span>

<span data-ttu-id="6fc9f-135">**bitmask**</span><span class="sxs-lookup"><span data-stu-id="6fc9f-135">**bitmask**</span></span>

<span data-ttu-id="6fc9f-136">Um valor numérico destinado a uma comparação de valor bit a bit com outros valores numéricos, geralmente para sinalizar opções em valores de parâmetro ou de retorno.</span><span class="sxs-lookup"><span data-stu-id="6fc9f-136">A numeric value intended for a bit-by-bit value comparison with other numeric values, typically to flag options in parameter or return values.</span></span> <span data-ttu-id="6fc9f-137">Geralmente, essa comparação é feita com operadores lógicos bit a bit, como **And** **e Or** no Visual Basic e **&** em **|** C++.</span><span class="sxs-lookup"><span data-stu-id="6fc9f-137">Usually this comparison is done with bitwise logical operators, such as **And** and **Or** in Visual Basic, **&** and **|** in C++.</span></span>

<span data-ttu-id="6fc9f-138">Por exemplo, os valores **fieldAttributeEnum** do ADO podem ser usados como bitmasks para determinar os atributos de um campo.</span><span class="sxs-lookup"><span data-stu-id="6fc9f-138">For example, the ADO **FieldAttributeEnum** values can be used as bitmasks to determine the attributes of a field.</span></span> <span data-ttu-id="6fc9f-139">Suponha que você quisesse determinar se um campo era atualizável.</span><span class="sxs-lookup"><span data-stu-id="6fc9f-139">Suppose you wanted to determine if a field was updateable.</span></span> <span data-ttu-id="6fc9f-140">Você pode testar isso com a expressão a seguir no Visual Basic:</span><span class="sxs-lookup"><span data-stu-id="6fc9f-140">You could test for this with the following expression in Visual Basic:</span></span>  
  

<span data-ttu-id="6fc9f-141">Se o resultado for VERDADEIRO, o campo será atualizável.</span><span class="sxs-lookup"><span data-stu-id="6fc9f-141">If the result is TRUE, then the field is updateable.</span></span>

<span data-ttu-id="6fc9f-142">**bookmark**</span><span class="sxs-lookup"><span data-stu-id="6fc9f-142">**bookmark**</span></span>

<span data-ttu-id="6fc9f-143">Um marcador que identifica exclusivamente uma linha dentro de um conjunto de linhas para que um usuário possa navegar rapidamente até ela.</span><span class="sxs-lookup"><span data-stu-id="6fc9f-143">A marker that uniquely identifies a row within a set of rows so that a user can quickly navigate to it.</span></span>

<span data-ttu-id="6fc9f-144">**objeto de negócios**</span><span class="sxs-lookup"><span data-stu-id="6fc9f-144">**business object**</span></span>

<span data-ttu-id="6fc9f-145">Um objeto que executa um conjunto definido de operações, como validação de dados ou lógica de regra comercial.</span><span class="sxs-lookup"><span data-stu-id="6fc9f-145">An object that performs a defined set of operations, such as data validation or business rule logic.</span></span> <span data-ttu-id="6fc9f-146">Os objetos de negócios geralmente residem na camada intermediária.</span><span class="sxs-lookup"><span data-stu-id="6fc9f-146">Business objects usually reside on the middle tier.</span></span>

<span data-ttu-id="6fc9f-147">**regra comercial**</span><span class="sxs-lookup"><span data-stu-id="6fc9f-147">**business rule**</span></span>

<span data-ttu-id="6fc9f-148">A combinação de edições de validação, verificações de logon, verificações de banco de dados, políticas e transformações de algoritmos que constituem o modo de fazer negócios de uma empresa.</span><span class="sxs-lookup"><span data-stu-id="6fc9f-148">The combination of validation edits, logon verifications, database lookups, policies, and algorithmic transformations that constitute an enterprise's way of doing business.</span></span> <span data-ttu-id="6fc9f-149">Também conhecido como *lógica de negócios.*</span><span class="sxs-lookup"><span data-stu-id="6fc9f-149">Also known as *business logic*.</span></span>

<span data-ttu-id="6fc9f-150">Retornar ao início</span><span class="sxs-lookup"><span data-stu-id="6fc9f-150">Return to top</span></span>

## <a name="c"></a><span data-ttu-id="6fc9f-151">C</span><span class="sxs-lookup"><span data-stu-id="6fc9f-151">C</span></span>

<span data-ttu-id="6fc9f-152">**calculated expression**</span><span class="sxs-lookup"><span data-stu-id="6fc9f-152">**calculated expression**</span></span>

<span data-ttu-id="6fc9f-153">Uma expressão que não é constante, mas cujo valor depende de outros valores.</span><span class="sxs-lookup"><span data-stu-id="6fc9f-153">An expression that is not constant, but whose value depends upon other values.</span></span> <span data-ttu-id="6fc9f-154">Para ser avaliada, uma expressão calculada deve obter e calcular valores de outras fontes, normalmente em outros campos ou linhas.</span><span class="sxs-lookup"><span data-stu-id="6fc9f-154">To be evaluated, a calculated expression must obtain and compute values from other sources, typically in other fields or rows.</span></span>

<span data-ttu-id="6fc9f-155">**capítulo**</span><span class="sxs-lookup"><span data-stu-id="6fc9f-155">**chapter**</span></span>

<span data-ttu-id="6fc9f-156">Uma referência a um intervalo de linhas de uma fonte de dados.</span><span class="sxs-lookup"><span data-stu-id="6fc9f-156">A reference to a range of rows from a data source.</span></span> <span data-ttu-id="6fc9f-157">No ADO, um capítulo é normalmente uma referência a outro **Recordset.**</span><span class="sxs-lookup"><span data-stu-id="6fc9f-157">In ADO, a chapter is typically a reference to another **Recordset**.</span></span>

<span data-ttu-id="6fc9f-158">As colunas de capítulo permitem definir uma relação *parent-child* em que *parent* representa o **Recordset** contendo a coluna de capítulo, e *child* é o **Recordset** representado pelo capítulo.</span><span class="sxs-lookup"><span data-stu-id="6fc9f-158">Chapter columns make it possible to define a *parent-child* relationship where the *parent* is the **Recordset** containing the chapter column and the *child* is the **Recordset** represented by the chapter.</span></span>

<span data-ttu-id="6fc9f-159">**chapter-alias**</span><span class="sxs-lookup"><span data-stu-id="6fc9f-159">**chapter-alias**</span></span>

<span data-ttu-id="6fc9f-160">Um alias que se refere à coluna anexada ao pai.</span><span class="sxs-lookup"><span data-stu-id="6fc9f-160">An alias that refers to the column appended to the parent.</span></span>

<span data-ttu-id="6fc9f-161">**conjunto de caracteres**</span><span class="sxs-lookup"><span data-stu-id="6fc9f-161">**character set**</span></span>

<span data-ttu-id="6fc9f-162">Um mapeamento de um conjunto de caracteres para seus valores numéricos.</span><span class="sxs-lookup"><span data-stu-id="6fc9f-162">A mapping of a set of characters to their numeric values.</span></span> <span data-ttu-id="6fc9f-163">Por exemplo, Unicode é um conjunto de caracteres de 16 bits capaz de codificar todos os caracteres conhecidos e usado como um padrão mundial de codificação de caracteres.</span><span class="sxs-lookup"><span data-stu-id="6fc9f-163">For example, Unicode is a 16-bit character set capable of encoding all known characters and used as a worldwide character-encoding standard.</span></span>

<span data-ttu-id="6fc9f-164">**filho**</span><span class="sxs-lookup"><span data-stu-id="6fc9f-164">**child**</span></span>

<span data-ttu-id="6fc9f-165">O lado dependente de uma relação hierárquica.</span><span class="sxs-lookup"><span data-stu-id="6fc9f-165">The dependent side of a hierarchical relationship.</span></span> <span data-ttu-id="6fc9f-166">Um filho é um nó em uma estrutura hierárquica que tem outro nó acima dele (mais próximo da raiz).</span><span class="sxs-lookup"><span data-stu-id="6fc9f-166">A child is a node in a hierarchical structure that has another node above it (closer to the root).</span></span> <span data-ttu-id="6fc9f-167">Consulte também **child-alias**, **relação pai-filho**, **pai**.</span><span class="sxs-lookup"><span data-stu-id="6fc9f-167">See also **child-alias**, **parent-child relationship**, **parent**.</span></span>

<span data-ttu-id="6fc9f-168">**child-alias**</span><span class="sxs-lookup"><span data-stu-id="6fc9f-168">**child-alias**</span></span>

<span data-ttu-id="6fc9f-169">Um alias que se refere ao filho.</span><span class="sxs-lookup"><span data-stu-id="6fc9f-169">An alias that refers to the child.</span></span> <span data-ttu-id="6fc9f-170">Consulte também **alias**, **filho**.</span><span class="sxs-lookup"><span data-stu-id="6fc9f-170">See also **alias**, **child**.</span></span>

<span data-ttu-id="6fc9f-171">**CLSID (identificador de classe)**</span><span class="sxs-lookup"><span data-stu-id="6fc9f-171">**CLSID (class identifier)**</span></span>

<span data-ttu-id="6fc9f-172">Um identificador universal exclusivo (UUID) que identifica um componente COM.</span><span class="sxs-lookup"><span data-stu-id="6fc9f-172">A universally unique identifier (UUID) that identifies a COM component.</span></span> <span data-ttu-id="6fc9f-173">Cada componente COM tem seu CLSID no Registro do Windows para que possa ser carregado por outros aplicativos.</span><span class="sxs-lookup"><span data-stu-id="6fc9f-173">Each COM component has its CLSID in the Windows Registry so that it can be loaded by other applications.</span></span> <span data-ttu-id="6fc9f-174">Consulte também **ProgID**, **COM**.</span><span class="sxs-lookup"><span data-stu-id="6fc9f-174">See also **ProgID**, **COM**.</span></span>

<span data-ttu-id="6fc9f-175">**camada do cliente**</span><span class="sxs-lookup"><span data-stu-id="6fc9f-175">**client tier**</span></span>

<span data-ttu-id="6fc9f-176">Uma camada lógica de um sistema distribuído que normalmente apresenta dados e processa a entrada do usuário, às vezes chamado de *front-end.*</span><span class="sxs-lookup"><span data-stu-id="6fc9f-176">A logical layer of a distributed system that typically presents data to and processes input from the user, sometimes referred to as the *front end*.</span></span> <span data-ttu-id="6fc9f-177">Normalmente, a camada do cliente solicita dados de um servidor com base na entrada e, em seguida, formatar e exibir o resultado.</span><span class="sxs-lookup"><span data-stu-id="6fc9f-177">Usually, the client tier requests data from a server based on input, and then formats and displays the result.</span></span> <span data-ttu-id="6fc9f-178">Consulte também camada **intermediária**, **camada de fonte de dados**, aplicativo **distribuído**.</span><span class="sxs-lookup"><span data-stu-id="6fc9f-178">See also **middle tier**, **data source tier**, **distributed application**.</span></span>

<span data-ttu-id="6fc9f-179">**COM (Component Object Model)**</span><span class="sxs-lookup"><span data-stu-id="6fc9f-179">**COM (Component Object Model)**</span></span>

<span data-ttu-id="6fc9f-180">Um padrão binário que permite que objetos interoperem em um ambiente em rede, independentemente do idioma em que foram desenvolvidos ou em quais computadores residem.</span><span class="sxs-lookup"><span data-stu-id="6fc9f-180">A binary standard that enables objects to interoperate in a networked environment regardless of the language in which they were developed or on which computers they reside.</span></span> <span data-ttu-id="6fc9f-181">Tecnologias baseadas em COM incluem Controles ActiveX, Automação e vinculação e incorporação de objetos (OLE).</span><span class="sxs-lookup"><span data-stu-id="6fc9f-181">COM-based technologies include ActiveX Controls, Automation, and object linking and embedding (OLE).</span></span> <span data-ttu-id="6fc9f-182">O COM permite que um objeto exponha sua funcionalidade a outros componentes e hospede aplicativos.</span><span class="sxs-lookup"><span data-stu-id="6fc9f-182">COM allows an object to expose its functionality to other components and to host applications.</span></span> <span data-ttu-id="6fc9f-183">Ele define como o objeto se expõe e como essa exposição funciona em processos e em redes.</span><span class="sxs-lookup"><span data-stu-id="6fc9f-183">It defines both how the object exposes itself and how this exposure works across processes and across networks.</span></span> <span data-ttu-id="6fc9f-184">COM também define o ciclo de vida do objeto.</span><span class="sxs-lookup"><span data-stu-id="6fc9f-184">COM also defines the object's life cycle.</span></span>

<span data-ttu-id="6fc9f-185">**Componente COM**</span><span class="sxs-lookup"><span data-stu-id="6fc9f-185">**COM component**</span></span>

<span data-ttu-id="6fc9f-186">Arquivo binário — como .dll, .ocx e alguns arquivos .exe — que oferece suporte ao padrão COM para fornecer objetos.</span><span class="sxs-lookup"><span data-stu-id="6fc9f-186">Binary file — such as .dll, .ocx, and some .exe files — that supports the COM standard for providing objects.</span></span> <span data-ttu-id="6fc9f-187">Esse arquivo contém código para uma ou mais armas de classe, classes COM, mecanismos de entrada do Registro, código de carregamento e assim por diante.</span><span class="sxs-lookup"><span data-stu-id="6fc9f-187">Such a file contains code for one or more class factories, COM classes, registry-entry mechanisms, loading code, and so on.</span></span>

<span data-ttu-id="6fc9f-188">**operador de comparação**</span><span class="sxs-lookup"><span data-stu-id="6fc9f-188">**comparison operator**</span></span>

<span data-ttu-id="6fc9f-189">Um operador que compara duas expressões e retorna um valor booleano.</span><span class="sxs-lookup"><span data-stu-id="6fc9f-189">An operator that compares two expressions and returns a Boolean value.</span></span>

<span data-ttu-id="6fc9f-190">Um parâmetro de critério que pode ser expresso como " \> " (maior que), \< " " (menor que), "=" (igual), " \> =" (maior ou igual), " \< =" (menor ou igual), \< \> " " (diferente) ou "like" (correspondência de padrão).</span><span class="sxs-lookup"><span data-stu-id="6fc9f-190">A criteria parameter that may be expressed as "\>" (greater than), "\<" (less than), "=" (equal), "\>=" (greater than or equal), "\<=" (less than or equal), "\<\>" (not equal), or "like" (pattern matching).</span></span>

<span data-ttu-id="6fc9f-191">**component**</span><span class="sxs-lookup"><span data-stu-id="6fc9f-191">**component**</span></span>

<span data-ttu-id="6fc9f-192">Um objeto que encapsula dados e códigos e fornece um conjunto bem especificado de serviços publicamente disponíveis.</span><span class="sxs-lookup"><span data-stu-id="6fc9f-192">An object that encapsulates both data and code, and provides a well-specified set of publicly available services.</span></span>

<span data-ttu-id="6fc9f-193">**arquivo composto**</span><span class="sxs-lookup"><span data-stu-id="6fc9f-193">**compound file**</span></span>

<span data-ttu-id="6fc9f-194">Uma implementação de armazenamento estruturado com COM para arquivos.</span><span class="sxs-lookup"><span data-stu-id="6fc9f-194">An implementation of COM structured storage for files.</span></span> <span data-ttu-id="6fc9f-195">Um arquivo composto armazena objetos separados em um único arquivo estruturado que consiste em dois elementos principais: objetos de armazenamento e objetos de fluxo.</span><span class="sxs-lookup"><span data-stu-id="6fc9f-195">A compound file stores separate objects in a single, structured file consisting of two main elements: storage objects and stream objects.</span></span> <span data-ttu-id="6fc9f-196">Juntos, eles funcionam como um sistema de arquivos em um arquivo.</span><span class="sxs-lookup"><span data-stu-id="6fc9f-196">Together, they function like a file system within a file.</span></span> <span data-ttu-id="6fc9f-197">Para obter mais informações, consulte Arquivos Compostos no SDK da Plataforma Microsoft.</span><span class="sxs-lookup"><span data-stu-id="6fc9f-197">For more information, see Compound Files in the Microsoft Platform SDK.</span></span>

<span data-ttu-id="6fc9f-198">Vários arquivos individuais vinculados em um arquivo físico.</span><span class="sxs-lookup"><span data-stu-id="6fc9f-198">A number of individual files bound together in one physical file.</span></span> <span data-ttu-id="6fc9f-199">Cada arquivo individual em um arquivo composto pode ser acessado como se fosse um único arquivo físico.</span><span class="sxs-lookup"><span data-stu-id="6fc9f-199">Each individual file in a compound file can be accessed as if it were a single physical file.</span></span>

<span data-ttu-id="6fc9f-200">**constante**</span><span class="sxs-lookup"><span data-stu-id="6fc9f-200">**constant**</span></span>

<span data-ttu-id="6fc9f-201">Um valor numérico ou de cadeia de caracteres que não muda.</span><span class="sxs-lookup"><span data-stu-id="6fc9f-201">A numeric or string value that does not change.</span></span> <span data-ttu-id="6fc9f-202">Enumerações do ADO nomeadas (constantes enumeradas) podem ser usadas em seu código em vez de valores reais, por exemplo, **adUseClient** é uma constante cujo valor é 3.</span><span class="sxs-lookup"><span data-stu-id="6fc9f-202">Named ADO enumerations (enumerated constants) can be used in your code instead of actual values, for example, **adUseClient** is a constant whose value is 3.</span></span> <span data-ttu-id="6fc9f-203">(Const adUseClient = 3).</span><span class="sxs-lookup"><span data-stu-id="6fc9f-203">(Const adUseClient = 3).</span></span> <span data-ttu-id="6fc9f-204">Consulte também **enumeração**.</span><span class="sxs-lookup"><span data-stu-id="6fc9f-204">See also **enumeration**.</span></span>

<span data-ttu-id="6fc9f-205">**cursor**</span><span class="sxs-lookup"><span data-stu-id="6fc9f-205">**cursor**</span></span>

<span data-ttu-id="6fc9f-206">Um elemento de banco de dados que controla a navegação de registros, a capacidade de atualização de dados e a visibilidade das alterações feitas no banco de dados por outros usuários.</span><span class="sxs-lookup"><span data-stu-id="6fc9f-206">A database element that controls record navigation, updateability of data, and the visibility of changes made to the database by other users.</span></span>

<span data-ttu-id="6fc9f-207">Retornar ao início</span><span class="sxs-lookup"><span data-stu-id="6fc9f-207">Return to top</span></span>

## <a name="d"></a><span data-ttu-id="6fc9f-208">D</span><span class="sxs-lookup"><span data-stu-id="6fc9f-208">D</span></span>

<span data-ttu-id="6fc9f-209">**vinculação de dados**</span><span class="sxs-lookup"><span data-stu-id="6fc9f-209">**data binding**</span></span>

<span data-ttu-id="6fc9f-210">O processo de associação dos objetos ou controles de um aplicativo a uma fonte de dados.</span><span class="sxs-lookup"><span data-stu-id="6fc9f-210">The process of associating the objects or controls of an application to a data source.</span></span> <span data-ttu-id="6fc9f-211">Um controle associado a uma fonte de dados é chamado de controle *vinculado a dados.*</span><span class="sxs-lookup"><span data-stu-id="6fc9f-211">A control associated with a data source is called a *data-bound control*.</span></span>

<span data-ttu-id="6fc9f-212">O conteúdo de um controle vinculado a dados está associado a valores de um banco de dados.</span><span class="sxs-lookup"><span data-stu-id="6fc9f-212">The contents of a data-bound control are associated with values from a database.</span></span> <span data-ttu-id="6fc9f-213">Por exemplo, um controle de grade vinculado a um objeto **Recordset** pode ser atualizado quando as linhas do **Recordset** são atualizadas.</span><span class="sxs-lookup"><span data-stu-id="6fc9f-213">For example, a grid control that is bound to a **Recordset** object can be updated when the rows in the **Recordset** are updated.</span></span> <span data-ttu-id="6fc9f-214">Quando novos valores são recuperados pelo **Recordset,** novos valores são exibidos na grade.</span><span class="sxs-lookup"><span data-stu-id="6fc9f-214">When new values are retrieved by the **Recordset**, new values are displayed in the grid.</span></span>

<span data-ttu-id="6fc9f-215">**provedor de dados**</span><span class="sxs-lookup"><span data-stu-id="6fc9f-215">**data provider**</span></span>

<span data-ttu-id="6fc9f-216">Software que expõe dados a um aplicativo ADO diretamente ou por meio de um provedor de serviços.</span><span class="sxs-lookup"><span data-stu-id="6fc9f-216">Software that exposes data to an ADO application either directly or via a service provider.</span></span> <span data-ttu-id="6fc9f-217">Consulte também provedor **de serviços.**</span><span class="sxs-lookup"><span data-stu-id="6fc9f-217">See also **service provider**.</span></span>

<span data-ttu-id="6fc9f-218">**data shaping**</span><span class="sxs-lookup"><span data-stu-id="6fc9f-218">**data shaping**</span></span>

<span data-ttu-id="6fc9f-219">Uma técnica que faz uso de uma sintaxe formalizada (chamada de linguagem **Shape)** para definir um objeto **Recordset** especializado (chamado de **Recordset** com formato) que contém não apenas dados, mas também referências a outros objetos **Recordset** e/ou valores calculados com base nesses outros objetos **Recordset.**</span><span class="sxs-lookup"><span data-stu-id="6fc9f-219">A technique which makes use of a formalized syntax (called **Shape language**) to define a specialized **Recordset** object (called a **shaped Recordset**) that contains not just data, but also references to other **Recordset** objects and/or computed values based on those other **Recordset** objects.</span></span>

<span data-ttu-id="6fc9f-220">**camada de fonte de dados**</span><span class="sxs-lookup"><span data-stu-id="6fc9f-220">**data source tier**</span></span>

<span data-ttu-id="6fc9f-221">Uma camada lógica de um sistema distribuído que representa um computador executando um DBMS, como um banco de dados do SQL Server.</span><span class="sxs-lookup"><span data-stu-id="6fc9f-221">A logical layer of a distributed system that represents a computer running a DBMS, such as an SQL Server database.</span></span> <span data-ttu-id="6fc9f-222">Consulte também a **camada do cliente,** **camada intermediária,** **aplicativo distribuído.**</span><span class="sxs-lookup"><span data-stu-id="6fc9f-222">See also **client tier**, **middle tier**, **distributed application**.</span></span>

<span data-ttu-id="6fc9f-223">**DCOM**</span><span class="sxs-lookup"><span data-stu-id="6fc9f-223">**DCOM**</span></span>

<span data-ttu-id="6fc9f-224">Um protocolo de transmissão que permite que os componentes COM se comuniquem diretamente uns com os outros em uma rede.</span><span class="sxs-lookup"><span data-stu-id="6fc9f-224">A wire protocol that enables COM components to communicate directly with each other across a network.</span></span> <span data-ttu-id="6fc9f-225">Consulte também **COM**, **componente**.</span><span class="sxs-lookup"><span data-stu-id="6fc9f-225">See also **COM**, **component**.</span></span>

<span data-ttu-id="6fc9f-226">**DDL (Linguagem de Definição de Dados)**</span><span class="sxs-lookup"><span data-stu-id="6fc9f-226">**DDL (Data Definition Language)**</span></span>

<span data-ttu-id="6fc9f-227">As instruções no SQL que definem, em vez de manipular, dados.</span><span class="sxs-lookup"><span data-stu-id="6fc9f-227">Those statements in SQL that define, as opposed to manipulate, data.</span></span> <span data-ttu-id="6fc9f-228">O esquema de um banco de dados é criado ou modificado com DDL.</span><span class="sxs-lookup"><span data-stu-id="6fc9f-228">The schema of a database is created or modified with DDL.</span></span> <span data-ttu-id="6fc9f-229">Por exemplo, **CREATE TABLE**, **CREATE INDEX**, **GRANT** e **REVOKE são** instruções DDL sql.</span><span class="sxs-lookup"><span data-stu-id="6fc9f-229">For example, **CREATE TABLE**, **CREATE INDEX**, **GRANT**, and **REVOKE** are SQL DDL statements.</span></span>

<span data-ttu-id="6fc9f-230">**fluxo padrão**</span><span class="sxs-lookup"><span data-stu-id="6fc9f-230">**default stream**</span></span>

<span data-ttu-id="6fc9f-231">Um fluxo de texto ou binário (representado por um objeto **Stream)** que é associado a objetos **Record** ou **Recordset** ao usar determinados provedores OLE DB, como o Microsoft OLE DB Provider for Internet Publishing.</span><span class="sxs-lookup"><span data-stu-id="6fc9f-231">A text or binary stream (represented by a **Stream** object) that is associated with **Record** or **Recordset** objects when using certain OLE DB providers, such as the Microsoft OLE DB Provider for Internet Publishing.</span></span> <span data-ttu-id="6fc9f-232">O fluxo padrão normalmente contém o conteúdo de um arquivo, como o código HTML para a raiz de um site.</span><span class="sxs-lookup"><span data-stu-id="6fc9f-232">The default stream typically contains the contents of a file such as the HTML code for the root of a website.</span></span>

<span data-ttu-id="6fc9f-233">**aplicativo distribuído**</span><span class="sxs-lookup"><span data-stu-id="6fc9f-233">**distributed application**</span></span>

<span data-ttu-id="6fc9f-234">Um programa escrito para que o processamento possa ser dividido entre vários computadores em uma rede.</span><span class="sxs-lookup"><span data-stu-id="6fc9f-234">A program written so that the processing can be divided across multiple computers over a network.</span></span> <span data-ttu-id="6fc9f-235">Normalmente, um aplicativo distribuído é dividido em apresentação, lógica de negócios e camadas de armazenamento de dados ou *camadas.*</span><span class="sxs-lookup"><span data-stu-id="6fc9f-235">Typically, a distributed application is divided into presentation, business logic, and data store layers, or *tiers*.</span></span> <span data-ttu-id="6fc9f-236">Consulte também a **camada do cliente**, camada **intermediária**, camada de fonte **de dados.**</span><span class="sxs-lookup"><span data-stu-id="6fc9f-236">See also **client tier**, **middle tier**, **data source tier**.</span></span>

<span data-ttu-id="6fc9f-237">**Recordset desconectado**</span><span class="sxs-lookup"><span data-stu-id="6fc9f-237">**disconnected Recordset**</span></span>

<span data-ttu-id="6fc9f-238">Um **objeto Recordset** em um cache de cliente que não tem mais uma conexão ao vivo com o servidor.</span><span class="sxs-lookup"><span data-stu-id="6fc9f-238">A **Recordset** object in a client cache that no longer has a live connection to the server.</span></span> <span data-ttu-id="6fc9f-239">Se a fonte de dados original precisar ser acessada novamente por algum motivo, como atualizar dados, a conexão deverá ser estabelecida novamente.</span><span class="sxs-lookup"><span data-stu-id="6fc9f-239">If the original data source needs to be accessed again for some reason, such as updating data, the connection must be re-established.</span></span> <span data-ttu-id="6fc9f-240">No entanto, as coleções, as propriedades e os métodos de um **Recordset** desconectado ainda podem ser acessados.</span><span class="sxs-lookup"><span data-stu-id="6fc9f-240">However, the collections, properties, and methods of a disconnected **Recordset** can still be accessed.</span></span>

<span data-ttu-id="6fc9f-241">**DLL (biblioteca de vínculo dinâmico)**</span><span class="sxs-lookup"><span data-stu-id="6fc9f-241">**DLL (dynamic-link library)**</span></span>

<span data-ttu-id="6fc9f-242">Um arquivo que contém uma ou mais funções compiladas, vinculadas e armazenadas separadamente dos processos que as utilizam.</span><span class="sxs-lookup"><span data-stu-id="6fc9f-242">A file that contains one or more functions that are compiled, linked, and stored separately from the processes that use them.</span></span> <span data-ttu-id="6fc9f-243">O sistema operacional mapeia as DLLs para o espaço de endereço do processo de chamada quando o processo é iniciando ou enquanto ele está em execução.</span><span class="sxs-lookup"><span data-stu-id="6fc9f-243">The operating system maps the DLLs into the address space of the calling process when the process is starting, or while it is running.</span></span>

<span data-ttu-id="6fc9f-244">**DML (Linguagem de Manipulação de Dados)**</span><span class="sxs-lookup"><span data-stu-id="6fc9f-244">**DML (Data Manipulation Language)**</span></span>

<span data-ttu-id="6fc9f-245">As instruções no SQL que manipulam, em vez de definir, dados.</span><span class="sxs-lookup"><span data-stu-id="6fc9f-245">Those statements in SQL that manipulate, as opposed to define, data.</span></span> <span data-ttu-id="6fc9f-246">Os valores em um banco de dados são selecionados e modificados com DML.</span><span class="sxs-lookup"><span data-stu-id="6fc9f-246">The values in a database are selected and modified with DML.</span></span> <span data-ttu-id="6fc9f-247">Por exemplo, **INSERT**, **UPDATE,** **DELETE** e **SELECT são** instruções DML sql.</span><span class="sxs-lookup"><span data-stu-id="6fc9f-247">For example, **INSERT**, **UPDATE**, **DELETE**, and **SELECT** are SQL DML statements.</span></span>

<span data-ttu-id="6fc9f-248">**provedor de fonte de documentos**</span><span class="sxs-lookup"><span data-stu-id="6fc9f-248">**document source provider**</span></span>

<span data-ttu-id="6fc9f-249">Uma classe especial de provedores que gerenciam pastas e documentos.</span><span class="sxs-lookup"><span data-stu-id="6fc9f-249">A special class of providers that manage folders and documents.</span></span> <span data-ttu-id="6fc9f-250">Quando um documento é representado por um objeto **Record** ou uma pasta de documentos é representada por um objeto **Recordset,** o provedor de origem do documento preenche esses objetos com um conjunto exclusivo de campos que descrevem características do documento, em vez do próprio documento real.</span><span class="sxs-lookup"><span data-stu-id="6fc9f-250">When a document is represented by a **Record** object, or a folder of documents is represented by a **Recordset** object, the document source provider populates those objects with a unique set of fields that describe characteristics of the document, instead of the actual document itself.</span></span> <span data-ttu-id="6fc9f-251">Consulte também o **registro de recursos.**</span><span class="sxs-lookup"><span data-stu-id="6fc9f-251">See also **resource record**.</span></span>

<span data-ttu-id="6fc9f-252">**DSN (nome da fonte de dados)**</span><span class="sxs-lookup"><span data-stu-id="6fc9f-252">**DSN (data source name)**</span></span>

<span data-ttu-id="6fc9f-253">A coleção de informações usadas para conectar seu aplicativo a um banco de dados ODBC específico.</span><span class="sxs-lookup"><span data-stu-id="6fc9f-253">The collection of information used to connect your application to a particular ODBC database.</span></span> <span data-ttu-id="6fc9f-254">O Gerenciador de Driver ODBC usa essas informações para criar uma conexão com o banco de dados.</span><span class="sxs-lookup"><span data-stu-id="6fc9f-254">The ODBC Driver Manager uses this information to create a connection to the database.</span></span> <span data-ttu-id="6fc9f-255">Um DSN pode ser armazenado em um arquivo (um arquivo DSN) ou no Registro do Windows (um DSN de computador).</span><span class="sxs-lookup"><span data-stu-id="6fc9f-255">A DSN can be stored in a file (a file DSN) or in the Windows Registry (a machine DSN).</span></span>

<span data-ttu-id="6fc9f-256">**propriedade dinâmica**</span><span class="sxs-lookup"><span data-stu-id="6fc9f-256">**dynamic property**</span></span>

<span data-ttu-id="6fc9f-257">Uma propriedade específica de um provedor de dados ou do serviço de cursor.</span><span class="sxs-lookup"><span data-stu-id="6fc9f-257">A property specific to a data provider or the cursor service.</span></span> <span data-ttu-id="6fc9f-258">A **coleção Properties** de um objeto é preenchida com elas automaticamente ("dinamicamente").</span><span class="sxs-lookup"><span data-stu-id="6fc9f-258">The **Properties** collection of an object is populated with these automatically ("dynamically").</span></span> <span data-ttu-id="6fc9f-259">Um objeto não tem propriedades dinâmicas até que esteja conectado a uma fonte de dados por meio de um provedor de dados específico.</span><span class="sxs-lookup"><span data-stu-id="6fc9f-259">An object has no dynamic properties until it is connected to a data source through a particular data provider.</span></span> <span data-ttu-id="6fc9f-260">Consulte também **o provedor de dados**, **cursor**.</span><span class="sxs-lookup"><span data-stu-id="6fc9f-260">See also **data provider**, **cursor**.</span></span>

<span data-ttu-id="6fc9f-261">Retornar ao início</span><span class="sxs-lookup"><span data-stu-id="6fc9f-261">Return to top</span></span>

## <a name="e-i"></a><span data-ttu-id="6fc9f-262">E-I</span><span class="sxs-lookup"><span data-stu-id="6fc9f-262">E-I</span></span>

<span data-ttu-id="6fc9f-263">**enumeração**</span><span class="sxs-lookup"><span data-stu-id="6fc9f-263">**enumeration**</span></span>

<span data-ttu-id="6fc9f-264">Uma lista de constantes nomeadas.</span><span class="sxs-lookup"><span data-stu-id="6fc9f-264">A list of named constants.</span></span> <span data-ttu-id="6fc9f-265">Os valores enumerados não precisam ser exclusivos.</span><span class="sxs-lookup"><span data-stu-id="6fc9f-265">Enumerated values need not be unique.</span></span> <span data-ttu-id="6fc9f-266">No entanto, o nome de cada valor deve ser exclusivo dentro do escopo onde a enumeração é definida.</span><span class="sxs-lookup"><span data-stu-id="6fc9f-266">However the name of each value must be unique within the scope where the enumeration is defined.</span></span> <span data-ttu-id="6fc9f-267">No ADO, as enumerações são usadas para parâmetro numérico e valores de retorno, para adicionar significado ao código do ADO e para proteger o desenvolvedor dos valores numéricos (que podem mudar de uma versão para outra).</span><span class="sxs-lookup"><span data-stu-id="6fc9f-267">In ADO, enumerations are used for numeric parameter and return values, to add meaning to ADO code and to shield the developer from the numeric values (which may change from version to version).</span></span> <span data-ttu-id="6fc9f-268">Por exemplo, para abrir um **Recordset estático,** use o valor enumerado **adOpenStatic:**</span><span class="sxs-lookup"><span data-stu-id="6fc9f-268">For example, to open a static **Recordset**, use the **adOpenStatic** enumerated value:</span></span>  
  

<span data-ttu-id="6fc9f-269">Também conhecido como constante *enumerada*.</span><span class="sxs-lookup"><span data-stu-id="6fc9f-269">Also referred to as *enumerated constant*.</span></span> <span data-ttu-id="6fc9f-270">Consulte também **constante**.</span><span class="sxs-lookup"><span data-stu-id="6fc9f-270">See also **constant**.</span></span>

<span data-ttu-id="6fc9f-271">**evento**</span><span class="sxs-lookup"><span data-stu-id="6fc9f-271">**event**</span></span>

<span data-ttu-id="6fc9f-272">Uma ação reconhecida por um objeto, para a qual você pode escrever código para responder.</span><span class="sxs-lookup"><span data-stu-id="6fc9f-272">An action recognized by an object, for which you can write code to respond.</span></span> <span data-ttu-id="6fc9f-273">Os eventos podem ser gerados por execução de comando, conclusão de transação, navegação de recordset e atualizações de dados, entre outras ações.</span><span class="sxs-lookup"><span data-stu-id="6fc9f-273">Events can be generated by command execution, transaction completion, recordset navigation, and data updates, among other actions.</span></span> <span data-ttu-id="6fc9f-274">Consulte também o **manipulador de eventos.**</span><span class="sxs-lookup"><span data-stu-id="6fc9f-274">See also **event handler**.</span></span>

<span data-ttu-id="6fc9f-275">**manipulador de eventos**</span><span class="sxs-lookup"><span data-stu-id="6fc9f-275">**event handler**</span></span>

<span data-ttu-id="6fc9f-276">Um manipulador de eventos é o código que é executado quando ocorre um evento.</span><span class="sxs-lookup"><span data-stu-id="6fc9f-276">An event handler is the code that is executed when an event occurs.</span></span> <span data-ttu-id="6fc9f-277">Consulte também **evento**.</span><span class="sxs-lookup"><span data-stu-id="6fc9f-277">See also **event**.</span></span>

<span data-ttu-id="6fc9f-278">**handler**</span><span class="sxs-lookup"><span data-stu-id="6fc9f-278">**handler**</span></span>

<span data-ttu-id="6fc9f-279">Uma rotina que gerencia uma condição ou operação comum e relativamente simples, como recuperação de erros ou gerenciamento de dados.</span><span class="sxs-lookup"><span data-stu-id="6fc9f-279">A routine that manages a common and relatively simple condition or operation, such as error recovery or data management.</span></span>

<span data-ttu-id="6fc9f-280">**Recordset hierárquico**</span><span class="sxs-lookup"><span data-stu-id="6fc9f-280">**hierarchical Recordset**</span></span>

<span data-ttu-id="6fc9f-281">Um **Recordset** que contém outro **Recordset**.</span><span class="sxs-lookup"><span data-stu-id="6fc9f-281">A **Recordset** that contains another **Recordset**.</span></span> <span data-ttu-id="6fc9f-282">Consulte também **data shaping**, **capítulo**.</span><span class="sxs-lookup"><span data-stu-id="6fc9f-282">See also **data shaping**, **chapter**.</span></span>

<span data-ttu-id="6fc9f-283">Para obter mais informações, [consulte Acessando linhas em um recordset hierárquico](accessing-rows-in-a-hierarchical-recordset.md)</span><span class="sxs-lookup"><span data-stu-id="6fc9f-283">For more information, see [Accessing Rows in a Hierarchical Recordset](accessing-rows-in-a-hierarchical-recordset.md)</span></span>

<span data-ttu-id="6fc9f-284">**hierarchy**</span><span class="sxs-lookup"><span data-stu-id="6fc9f-284">**hierarchy**</span></span>

<span data-ttu-id="6fc9f-285">Em geral, uma hierarquia é uma estrutura classificada com níveis de nível superior e subordinados.</span><span class="sxs-lookup"><span data-stu-id="6fc9f-285">In general, a hierarchy is a ranked structure with a top level and subordinate levels.</span></span> <span data-ttu-id="6fc9f-286">No ADO, **recordsets** hierárquicos são usados para representar a relação pai-filho entre um registro e um capítulo.</span><span class="sxs-lookup"><span data-stu-id="6fc9f-286">In ADO, hierarchical **Recordsets** are used to represent the parent-child relationship between a record and a chapter.</span></span> <span data-ttu-id="6fc9f-287">Também no ADO, os **objetos Record** e **Stream** podem ser usados para acessar estruturas de árvore hierárquicas, como uma pasta e documentos.</span><span class="sxs-lookup"><span data-stu-id="6fc9f-287">Also in ADO, **Record** and **Stream** objects can be used to access hierarchical tree structures such as a folder and documents.</span></span> <span data-ttu-id="6fc9f-288">O ADO MD também inclui **objetos Hierarchy** para representar uma relação entre os níveis de uma dimensão em um cubo OLAP.</span><span class="sxs-lookup"><span data-stu-id="6fc9f-288">ADO MD also includes **Hierarchy** objects to represent a relationship between the levels of a dimension in an OLAP cube.</span></span> <span data-ttu-id="6fc9f-289">Consulte também **recordsets hierárquicos**, **relação pai-filho**, **capítulo**, **árvore**.</span><span class="sxs-lookup"><span data-stu-id="6fc9f-289">See also **hierarchical Recordsets**, **parent-child relationship**, **chapter**, **tree**.</span></span>

<span data-ttu-id="6fc9f-290">**ISAPI (Internet Server Application Programming Interface)**</span><span class="sxs-lookup"><span data-stu-id="6fc9f-290">**ISAPI (Internet Server Application Programming Interface)**</span></span>

<span data-ttu-id="6fc9f-291">Um conjunto de funções para servidores de Internet, como um Windows NT Server/Windows 2000 Server executando o Microsoft Internet Information Services (IIS).</span><span class="sxs-lookup"><span data-stu-id="6fc9f-291">A set of functions for Internet servers, such as a Windows NT Server/Windows 2000 Server running Microsoft Internet Information Services (IIS).</span></span>

<span data-ttu-id="6fc9f-292">Retornar ao início</span><span class="sxs-lookup"><span data-stu-id="6fc9f-292">Return to top</span></span>

## <a name="k-m"></a><span data-ttu-id="6fc9f-293">K-M</span><span class="sxs-lookup"><span data-stu-id="6fc9f-293">K-M</span></span>

<span data-ttu-id="6fc9f-294">**key**</span><span class="sxs-lookup"><span data-stu-id="6fc9f-294">**key**</span></span>

<span data-ttu-id="6fc9f-295">Uma coluna ou colunas em uma tabela que identificam exclusivamente uma linha; frequentemente usado para indexar uma tabela.</span><span class="sxs-lookup"><span data-stu-id="6fc9f-295">A column or columns in a table that uniquely identify a row; often used to index a table.</span></span>

<span data-ttu-id="6fc9f-296">**marshaling**</span><span class="sxs-lookup"><span data-stu-id="6fc9f-296">**marshaling**</span></span>

<span data-ttu-id="6fc9f-297">O processo de empacotamento, envio e descompactação de parâmetros do método de interface entre limites de thread ou processo.</span><span class="sxs-lookup"><span data-stu-id="6fc9f-297">The process of packaging, sending, and unpackaging interface method parameters across thread or process boundaries.</span></span>

<span data-ttu-id="6fc9f-298">**camada intermediária**</span><span class="sxs-lookup"><span data-stu-id="6fc9f-298">**middle tier**</span></span>

<span data-ttu-id="6fc9f-299">A camada lógica em um sistema distribuído entre uma interface do usuário ou um cliente Web e o banco de dados.</span><span class="sxs-lookup"><span data-stu-id="6fc9f-299">The logical layer in a distributed system between a user interface or web client and the database.</span></span> <span data-ttu-id="6fc9f-300">Normalmente, é aqui que os objetos de negócios são instaciados.</span><span class="sxs-lookup"><span data-stu-id="6fc9f-300">This is typically where business objects are instantiated.</span></span> <span data-ttu-id="6fc9f-301">A camada intermediária é um conjunto de regras e funções de negócios que geram e operam ao receber informações.</span><span class="sxs-lookup"><span data-stu-id="6fc9f-301">The middle tier is a collection of business rules and functions that generate and operate upon receiving information.</span></span> <span data-ttu-id="6fc9f-302">Eles fazem isso por meio de regras de negócios, que podem mudar com frequência e, portanto, são encapsuladas em componentes que são fisicamente separados da lógica do aplicativo em si.</span><span class="sxs-lookup"><span data-stu-id="6fc9f-302">They accomplish this through business rules, which can change frequently, and are thus encapsulated into components that are physically separate from the application logic itself.</span></span> <span data-ttu-id="6fc9f-303">Também conhecido como camada *de servidor de aplicativos.*</span><span class="sxs-lookup"><span data-stu-id="6fc9f-303">Also known as *application server tier*.</span></span> <span data-ttu-id="6fc9f-304">Consulte também **aplicativo distribuído, camada do** **cliente**, camada de fonte **de dados**.</span><span class="sxs-lookup"><span data-stu-id="6fc9f-304">See also **distributed application**, **client tier**, **data source tier**.</span></span>

<span data-ttu-id="6fc9f-305">**MIME (Extensão de Email da Internet multiuso)**</span><span class="sxs-lookup"><span data-stu-id="6fc9f-305">**MIME (Multi-purpose Internet Mail Extension)**</span></span>

<span data-ttu-id="6fc9f-306">Um protocolo de Internet originalmente desenvolvido para permitir a troca de mensagens de email com conteúdo rico em ambientes heterogêneos de rede, computador e email.</span><span class="sxs-lookup"><span data-stu-id="6fc9f-306">An Internet protocol originally developed to allow exchange of electronic mail messages with rich content across heterogeneous network, machine, and email environments.</span></span> <span data-ttu-id="6fc9f-307">Na prática, o MIME também foi adotado e estendido por aplicativos que não são de email.</span><span class="sxs-lookup"><span data-stu-id="6fc9f-307">In practice, MIME has also been adopted and extended by non-mail applications.</span></span>

<span data-ttu-id="6fc9f-308">MIME é um padrão que permite que dados binários sejam publicados e lidos na Internet.</span><span class="sxs-lookup"><span data-stu-id="6fc9f-308">MIME is a standard that allows binary data to be published and read on the Internet.</span></span> <span data-ttu-id="6fc9f-309">O header de um arquivo com dados binários contém o tipo MIME dos dados; Isso informa aos programas cliente (navegadores da Web e pacotes de email, por exemplo) que eles precisarão lidar com os dados de maneira diferente do que lidar com texto reto.</span><span class="sxs-lookup"><span data-stu-id="6fc9f-309">The header of a file with binary data contains the MIME type of the data; this informs client programs (web browsers and mail packages, for instance) that they will need to handle the data in a different way than they handle straight text.</span></span> <span data-ttu-id="6fc9f-310">Por exemplo, o header de um documento da Web que contém um gráfico JPEG contém o tipo MIME específico para o formato de arquivo JPEG.</span><span class="sxs-lookup"><span data-stu-id="6fc9f-310">For example, the header of a web document containing a JPEG graphic contains the MIME type specific to the JPEG file format.</span></span> <span data-ttu-id="6fc9f-311">Isso permite que um navegador exibir o arquivo com seu visualizador JPEG, se um estiver presente.</span><span class="sxs-lookup"><span data-stu-id="6fc9f-311">This allows a browser to display the file with its JPEG viewer, if one is present.</span></span>

<span data-ttu-id="6fc9f-312">Retornar ao início</span><span class="sxs-lookup"><span data-stu-id="6fc9f-312">Return to top</span></span>

## <a name="n-o"></a><span data-ttu-id="6fc9f-313">N-O</span><span class="sxs-lookup"><span data-stu-id="6fc9f-313">N-O</span></span>

<span data-ttu-id="6fc9f-314">**node**</span><span class="sxs-lookup"><span data-stu-id="6fc9f-314">**node**</span></span>

<span data-ttu-id="6fc9f-315">Um elemento em uma estrutura de árvore hierárquica.</span><span class="sxs-lookup"><span data-stu-id="6fc9f-315">An element in a hierarchical tree structure.</span></span> <span data-ttu-id="6fc9f-316">Um nó pode ser a raiz ou o filho de outro nó.</span><span class="sxs-lookup"><span data-stu-id="6fc9f-316">A node may be the root, or the child of another node.</span></span> <span data-ttu-id="6fc9f-317">Um nó também pode ser pai de vários filhos.</span><span class="sxs-lookup"><span data-stu-id="6fc9f-317">A node can also be the parent of multiple children.</span></span> <span data-ttu-id="6fc9f-318">Consulte também **hierarquia**, **árvore**, **raiz**, **filho**, **pai**.</span><span class="sxs-lookup"><span data-stu-id="6fc9f-318">See also **hierarchy**, **tree**, **root**, **child**, **parent**.</span></span>

<span data-ttu-id="6fc9f-319">**variável de objeto**</span><span class="sxs-lookup"><span data-stu-id="6fc9f-319">**object variable**</span></span>

<span data-ttu-id="6fc9f-320">Uma variável que contém uma referência para um objeto.</span><span class="sxs-lookup"><span data-stu-id="6fc9f-320">A variable that contains a reference to an object.</span></span> <span data-ttu-id="6fc9f-321">Por exemplo, objCustomObject é uma variável que aponta para um objeto do tipo CustomObject:</span><span class="sxs-lookup"><span data-stu-id="6fc9f-321">For example, objCustomObject is a variable that points to an object of type CustomObject:</span></span>  
  
<span data-ttu-id="6fc9f-322">é uma variável que aponta para um objeto do tipo CustomObject:</span><span class="sxs-lookup"><span data-stu-id="6fc9f-322">is a variable that points to an object of type CustomObject:</span></span>  
  
<span data-ttu-id="6fc9f-323">Set objCustomObject = CreateObject(adodb. Recordset)</span><span class="sxs-lookup"><span data-stu-id="6fc9f-323">Set objCustomObject = CreateObject(adodb.Recordset)</span></span>

<span data-ttu-id="6fc9f-324">**ODBC**</span><span class="sxs-lookup"><span data-stu-id="6fc9f-324">**ODBC (Open Database Connectivity)**</span></span>

<span data-ttu-id="6fc9f-325">Uma interface de linguagem de programação padrão usada para se conectar a uma variedade de fontes de dados.</span><span class="sxs-lookup"><span data-stu-id="6fc9f-325">A standard programming language interface used to connect to a variety of data sources.</span></span> <span data-ttu-id="6fc9f-326">Isso geralmente é acessado por meio do Painel de Controle, onde nomes de fonte de dados (DSNs) podem ser atribuídos para usar drivers ODBC específicos.</span><span class="sxs-lookup"><span data-stu-id="6fc9f-326">This is usually accessed through Control Panel, where data source names (DSNs) can be assigned to use specific ODBC drivers.</span></span>

<span data-ttu-id="6fc9f-327">**OLE DB**</span><span class="sxs-lookup"><span data-stu-id="6fc9f-327">**OLE DB**</span></span>

<span data-ttu-id="6fc9f-328">Um conjunto de interfaces que expõem dados de uma variedade de fontes usando COM.</span><span class="sxs-lookup"><span data-stu-id="6fc9f-328">A set of interfaces that expose data from a variety of sources using COM.</span></span> <span data-ttu-id="6fc9f-329">As interfaces OLE DB fornecem aplicativos com acesso uniforme a dados armazenados em diversas fontes de informações.</span><span class="sxs-lookup"><span data-stu-id="6fc9f-329">OLE DB interfaces provide applications with uniform access to data stored in diverse information sources.</span></span> <span data-ttu-id="6fc9f-330">Essas interfaces suportam a quantidade de funcionalidade DBMS apropriada à fonte de dados, permitindo que ela compartilhe seus dados.</span><span class="sxs-lookup"><span data-stu-id="6fc9f-330">These interfaces support the amount of DBMS functionality appropriate to the data source, enabling it to share its data.</span></span> <span data-ttu-id="6fc9f-331">Consulte também **COM**.</span><span class="sxs-lookup"><span data-stu-id="6fc9f-331">See also **COM**.</span></span>

<span data-ttu-id="6fc9f-332">**bloqueio otimista**</span><span class="sxs-lookup"><span data-stu-id="6fc9f-332">**optimistic locking**</span></span>

<span data-ttu-id="6fc9f-333">Um tipo de bloqueio no qual a página de dados que contém um ou mais registros, incluindo o registro que está sendo editado, está indisponível para outros usuários somente enquanto o registro está sendo atualizado pelo método **Update,** mas está disponível antes e depois da chamada para **Atualizar.**</span><span class="sxs-lookup"><span data-stu-id="6fc9f-333">A type of locking in which the data page containing one or more records, including the record being edited, is unavailable to other users only while the record is being updated by the **Update** method, but is available before and after the call to **Update**.</span></span>

<span data-ttu-id="6fc9f-334">Bloqueio otimista é usado quando o objeto **Recordset** é aberto com o parâmetro **LockType** ou a propriedade definida como **adLockOptimistic** ou **adLockBatchOptimistic**.</span><span class="sxs-lookup"><span data-stu-id="6fc9f-334">Optimistic locking is used when the **Recordset** object is opened with the **LockType** parameter or property set to **adLockOptimistic** or **adLockBatchOptimistic**.</span></span> <span data-ttu-id="6fc9f-335">Consulte também **o bloqueio pessimista.**</span><span class="sxs-lookup"><span data-stu-id="6fc9f-335">See also **pessimistic locking**.</span></span>

<span data-ttu-id="6fc9f-336">**valor ordinal**</span><span class="sxs-lookup"><span data-stu-id="6fc9f-336">**ordinal value**</span></span>

<span data-ttu-id="6fc9f-337">O local numérico de um item dentro de um pedido.</span><span class="sxs-lookup"><span data-stu-id="6fc9f-337">The numeric location of an item within an order.</span></span> <span data-ttu-id="6fc9f-338">Em uma coleção ADO, o valor ordinal do primeiro item é zero (0).</span><span class="sxs-lookup"><span data-stu-id="6fc9f-338">In an ADO collection, the ordinal value of the first item is zero (0).</span></span> <span data-ttu-id="6fc9f-339">O próximo item é um (1) e assim por diante.</span><span class="sxs-lookup"><span data-stu-id="6fc9f-339">The next item is one (1), and so on.</span></span>

<span data-ttu-id="6fc9f-340">Retornar ao início</span><span class="sxs-lookup"><span data-stu-id="6fc9f-340">Return to top</span></span>

## <a name="p"></a><span data-ttu-id="6fc9f-341">P</span><span class="sxs-lookup"><span data-stu-id="6fc9f-341">P</span></span>

<span data-ttu-id="6fc9f-342">**comando parametrizado**</span><span class="sxs-lookup"><span data-stu-id="6fc9f-342">**parameterized command**</span></span>

<span data-ttu-id="6fc9f-343">Uma consulta ou comando que permite definir valores de parâmetro antes de o comando ser executado.</span><span class="sxs-lookup"><span data-stu-id="6fc9f-343">A query or command that allows you to set parameter values before the command is executed.</span></span> <span data-ttu-id="6fc9f-344">Por exemplo, uma cadeia de caracteres SQL pode ser parametrizada pela incorporação de marcadores de parâmetro na cadeia de caracteres SQL (designada pelo caractere '?').</span><span class="sxs-lookup"><span data-stu-id="6fc9f-344">For example, a SQL string can be parameterized by embedding parameter markers in the SQL string (designated by the '?' character).</span></span> <span data-ttu-id="6fc9f-345">Em seguida, o aplicativo especifica valores para cada parâmetro e executa o comando.</span><span class="sxs-lookup"><span data-stu-id="6fc9f-345">The application then specifies values for each parameter and executes the command.</span></span>

<span data-ttu-id="6fc9f-346">**primário**</span><span class="sxs-lookup"><span data-stu-id="6fc9f-346">**parent**</span></span>

<span data-ttu-id="6fc9f-347">O lado de controle de uma relação hierárquica.</span><span class="sxs-lookup"><span data-stu-id="6fc9f-347">The controlling side of a hierarchical relationship.</span></span> <span data-ttu-id="6fc9f-348">Em uma estrutura hierárquica, um pai tem um ou mais nós filho diretamente abaixo dela na hierarquia.</span><span class="sxs-lookup"><span data-stu-id="6fc9f-348">In a hierarchical structure, a parent has one or more child nodes directly beneath it in the hierarchy.</span></span> <span data-ttu-id="6fc9f-349">Consulte também **parent-alias**, **parent-child relationship**, **child**.</span><span class="sxs-lookup"><span data-stu-id="6fc9f-349">See also **parent-alias**, **parent-child relationship**, **child**.</span></span>

<span data-ttu-id="6fc9f-350">**parent-alias**</span><span class="sxs-lookup"><span data-stu-id="6fc9f-350">**parent-alias**</span></span>

<span data-ttu-id="6fc9f-351">Um alias que se refere ao pai.</span><span class="sxs-lookup"><span data-stu-id="6fc9f-351">An alias that refers to the parent.</span></span> <span data-ttu-id="6fc9f-352">Consulte também **alias**, **pai**.</span><span class="sxs-lookup"><span data-stu-id="6fc9f-352">See also **alias**, **parent**.</span></span>

<span data-ttu-id="6fc9f-353">**relação pai-filho**</span><span class="sxs-lookup"><span data-stu-id="6fc9f-353">**parent-child relationship**</span></span>

<span data-ttu-id="6fc9f-354">Uma relação em uma estrutura hierárquica na qual o pai é um nível superior e associado diretamente a um ou mais filhos.</span><span class="sxs-lookup"><span data-stu-id="6fc9f-354">A relationship in a hierarchical structure in which the parent is one level higher and directly associated with one or more children.</span></span> <span data-ttu-id="6fc9f-355">Um filho está um nível mais baixo e deve ter um pai.</span><span class="sxs-lookup"><span data-stu-id="6fc9f-355">A child is one level lower and must have one parent.</span></span> <span data-ttu-id="6fc9f-356">Consulte também **pai**, **filho**.</span><span class="sxs-lookup"><span data-stu-id="6fc9f-356">See also **parent**, **child**.</span></span>

<span data-ttu-id="6fc9f-357">**persist**</span><span class="sxs-lookup"><span data-stu-id="6fc9f-357">**persist**</span></span>

<span data-ttu-id="6fc9f-358">Para salvar dados em um estado permanente, como salvar um **Recordset** em um arquivo.</span><span class="sxs-lookup"><span data-stu-id="6fc9f-358">To save data in a permanent state, such as saving a **Recordset** to a file.</span></span>

<span data-ttu-id="6fc9f-359">**bloqueio pessimista**</span><span class="sxs-lookup"><span data-stu-id="6fc9f-359">**pessimistic locking**</span></span>

<span data-ttu-id="6fc9f-360">Um tipo de bloqueio no qual a página que contém um ou mais registros, incluindo o registro que está sendo editado, não está disponível para outros usuários para garantir que uma atualização será feita.</span><span class="sxs-lookup"><span data-stu-id="6fc9f-360">A type of locking in which the page containing one or more records, including the record being edited, is unavailable to other users to ensure that an update will be made.</span></span> <span data-ttu-id="6fc9f-361">O comportamento de bloqueio pessimista é definido pelo provedor OLE DB.</span><span class="sxs-lookup"><span data-stu-id="6fc9f-361">Pessimistic locking behavior is defined by the OLE DB provider.</span></span> <span data-ttu-id="6fc9f-362">Normalmente, os registros são bloqueados na edição e permanecem indisponíveis até que **o método Update** seja concluído.</span><span class="sxs-lookup"><span data-stu-id="6fc9f-362">Typically, records are locked upon editing and remain unavailable until the **Update** method has completed.</span></span>

<span data-ttu-id="6fc9f-363">O bloqueio pessimista é habilitado quando o objeto **Recordset** é aberto com o parâmetro **LockType** ou a propriedade definida como **adLockPessimistic**.</span><span class="sxs-lookup"><span data-stu-id="6fc9f-363">Pessimistic locking is enabled when the **Recordset** object is opened with the **LockType** parameter or property set to **adLockPessimistic**.</span></span> <span data-ttu-id="6fc9f-364">Veja também **bloqueio otimista.**</span><span class="sxs-lookup"><span data-stu-id="6fc9f-364">See also **optimistic locking**.</span></span>

<span data-ttu-id="6fc9f-365">**pooling**</span><span class="sxs-lookup"><span data-stu-id="6fc9f-365">**pooling**</span></span>

<span data-ttu-id="6fc9f-366">Uma otimização de desempenho baseada no uso de coleções de recursos pré-alocados, como objetos ou conexões de banco de dados.</span><span class="sxs-lookup"><span data-stu-id="6fc9f-366">A performance optimization based on using collections of pre-allocated resources, such as objects or database connections.</span></span> <span data-ttu-id="6fc9f-367">É mais eficiente desenhar um recurso existente do pool do que criar um novo recurso.</span><span class="sxs-lookup"><span data-stu-id="6fc9f-367">It is more efficient to draw an existing resource from the pool than to create a new resource.</span></span>

<span data-ttu-id="6fc9f-368">**ProgID (identificador programático)**</span><span class="sxs-lookup"><span data-stu-id="6fc9f-368">**ProgID (programmatic identifier)**</span></span>

<span data-ttu-id="6fc9f-369">Um nome exclusivo mapeado para o Registro do Windows por um aplicativo COM.</span><span class="sxs-lookup"><span data-stu-id="6fc9f-369">A unique name mapped to the Windows registry by a COM application.</span></span> <span data-ttu-id="6fc9f-370">O ProgID de uma conexão do ADO é "ADODB. Connection".</span><span class="sxs-lookup"><span data-stu-id="6fc9f-370">The ProgID for an ADO Connection is "ADODB.Connection".</span></span> <span data-ttu-id="6fc9f-371">Consulte também **CLSID**, **COM**.</span><span class="sxs-lookup"><span data-stu-id="6fc9f-371">See also **CLSID**, **COM**.</span></span>

<span data-ttu-id="6fc9f-372">**proxy**</span><span class="sxs-lookup"><span data-stu-id="6fc9f-372">**proxy**</span></span>

<span data-ttu-id="6fc9f-373">Um objeto específico da interface que fornece o empacotamento do parâmetro e a comunicação necessária para um cliente chamar um objeto de aplicativo que está sendo executado em um ambiente de execução diferente, como em um thread diferente ou em outro processo.</span><span class="sxs-lookup"><span data-stu-id="6fc9f-373">An interface-specific object that provides the parameter marshaling and communication required for a client to call an application object that is running in a different execution environment, such as on a different thread or in another process.</span></span> <span data-ttu-id="6fc9f-374">O proxy está localizado com o cliente e se comunica com um stub correspondente que está localizado com o objeto de aplicativo que está sendo chamado.</span><span class="sxs-lookup"><span data-stu-id="6fc9f-374">The proxy is located with the client and communicates with a corresponding stub that is located with the application object that is being called.</span></span> <span data-ttu-id="6fc9f-375">Consulte também **stub**.</span><span class="sxs-lookup"><span data-stu-id="6fc9f-375">See also **stub**.</span></span>

<span data-ttu-id="6fc9f-376">Retornar ao início</span><span class="sxs-lookup"><span data-stu-id="6fc9f-376">Return to top</span></span>

## <a name="r"></a><span data-ttu-id="6fc9f-377">R</span><span class="sxs-lookup"><span data-stu-id="6fc9f-377">R</span></span>

<span data-ttu-id="6fc9f-378">**URL relativa**</span><span class="sxs-lookup"><span data-stu-id="6fc9f-378">**relative URL**</span></span>

<span data-ttu-id="6fc9f-379">Uma URL parcialmente qualificada que especifica um recurso na Internet ou em uma intranet cujo local é relativo a um ponto de partida especificado por uma URL absoluta ou um objeto connection do ADO equivalente.</span><span class="sxs-lookup"><span data-stu-id="6fc9f-379">A partially qualified URL that specifies a resource on the Internet or an intranet whose location is relative to a starting point specified by an absolute URL or equivalent ADO Connection object.</span></span> <span data-ttu-id="6fc9f-380">Na verdade, as URLs absolutas e relativas concatenadas restringem uma URL completa.</span><span class="sxs-lookup"><span data-stu-id="6fc9f-380">In effect, the concatenated absolute and relative URLs consitute a complete URL.</span></span> <span data-ttu-id="6fc9f-381">Consulte também **URL** e **URL absoluta.**</span><span class="sxs-lookup"><span data-stu-id="6fc9f-381">See also **URL** and **absolute URL**.</span></span>

<span data-ttu-id="6fc9f-382">**fonte de dados remota**</span><span class="sxs-lookup"><span data-stu-id="6fc9f-382">**remote data source**</span></span>

<span data-ttu-id="6fc9f-383">Uma fonte de dados que existe em outro computador, e não no sistema local (onde o aplicativo cliente é executado).</span><span class="sxs-lookup"><span data-stu-id="6fc9f-383">A data source that exists on a another computer, rather than on the local system (where the client application runs).</span></span>

<span data-ttu-id="6fc9f-384">**registro de recurso**</span><span class="sxs-lookup"><span data-stu-id="6fc9f-384">**resource record**</span></span>

<span data-ttu-id="6fc9f-385">Um registro de um provedor de fonte de documentos que contém campos para a definição e a descrição de uma pasta ou documento.</span><span class="sxs-lookup"><span data-stu-id="6fc9f-385">A record from a document source provider that contains fields for the definition and description of a folder or document.</span></span> <span data-ttu-id="6fc9f-386">O próprio documento não está contido no registro de recursos, mas normalmente pode ser acessado pelo fluxo padrão ou por um campo no registro de recursos que contém uma URL.</span><span class="sxs-lookup"><span data-stu-id="6fc9f-386">The document itself is not contained in the resource record but typically can be accessed by the default stream or a field in the resource record containing a URL.</span></span> <span data-ttu-id="6fc9f-387">Consulte também o **provedor de origem do documento,** **fluxo padrão,** **URL**.</span><span class="sxs-lookup"><span data-stu-id="6fc9f-387">See also **document source provider**, **default stream**, **URL**.</span></span>

<span data-ttu-id="6fc9f-388">**root**</span><span class="sxs-lookup"><span data-stu-id="6fc9f-388">**root**</span></span>

<span data-ttu-id="6fc9f-389">O nível superior em uma estrutura de árvore hierárquica.</span><span class="sxs-lookup"><span data-stu-id="6fc9f-389">The top level in a hierarchical tree structure.</span></span> <span data-ttu-id="6fc9f-390">O nó raiz não tem pais, mas pode ter filhos.</span><span class="sxs-lookup"><span data-stu-id="6fc9f-390">The root node has no parents, but may have children.</span></span> <span data-ttu-id="6fc9f-391">Consulte também **hierarquia**, **árvore**, **pai**, **filho**.</span><span class="sxs-lookup"><span data-stu-id="6fc9f-391">See also **hierarchy**, **tree**, **parent**, **child**.</span></span>

<span data-ttu-id="6fc9f-392">**rowset**</span><span class="sxs-lookup"><span data-stu-id="6fc9f-392">**rowset**</span></span>

<span data-ttu-id="6fc9f-393">Um conjunto de linhas de uma fonte de dados, todas com o mesmo esquema de campo.</span><span class="sxs-lookup"><span data-stu-id="6fc9f-393">A set of rows from a data source, all having the same field schema.</span></span> <span data-ttu-id="6fc9f-394">Um rowset pode representar todos ou alguns campos de uma tabela.</span><span class="sxs-lookup"><span data-stu-id="6fc9f-394">A rowset can represent all or some fields from a table.</span></span> <span data-ttu-id="6fc9f-395">Um rowset também pode representar uma tabela virtual, criada por uma consulta ou uma junção de duas ou mais tabelas.</span><span class="sxs-lookup"><span data-stu-id="6fc9f-395">A rowset can also represent a virtual table, created by a query or a join of two or more tables.</span></span> <span data-ttu-id="6fc9f-396">No ADO, os conjuntos de linhas são representados por **objetos Recordset.**</span><span class="sxs-lookup"><span data-stu-id="6fc9f-396">In ADO, rowsets are represented by **Recordset** objects.</span></span>

<span data-ttu-id="6fc9f-397">Retornar ao início</span><span class="sxs-lookup"><span data-stu-id="6fc9f-397">Return to top</span></span>

## <a name="s"></a><span data-ttu-id="6fc9f-398">S</span><span class="sxs-lookup"><span data-stu-id="6fc9f-398">S</span></span>

<span data-ttu-id="6fc9f-399">**schema**</span><span class="sxs-lookup"><span data-stu-id="6fc9f-399">**schema**</span></span>

<span data-ttu-id="6fc9f-400">Uma descrição de um banco de dados para o dbMS (sistema de gerenciamento de banco de dados), normalmente gerado usando o idioma de definição de dados fornecido pelo DBMS.</span><span class="sxs-lookup"><span data-stu-id="6fc9f-400">A description of a database to the database management system (DBMS), typically generated using the data definition language provided by the DBMS.</span></span> <span data-ttu-id="6fc9f-401">Um esquema define atributos do banco de dados, como tabelas, colunas e propriedades.</span><span class="sxs-lookup"><span data-stu-id="6fc9f-401">A schema defines attributes of the database, such as tables, columns, and properties.</span></span>

<span data-ttu-id="6fc9f-402">**scope**</span><span class="sxs-lookup"><span data-stu-id="6fc9f-402">**scope**</span></span>

<span data-ttu-id="6fc9f-403">O intervalo de referência para um objeto ou variável ou um intervalo de registros em uma exibição ou tabela.</span><span class="sxs-lookup"><span data-stu-id="6fc9f-403">The range of reference for an object or variable or a range of records in a view or table.</span></span> <span data-ttu-id="6fc9f-404">Por exemplo, as variáveis locais podem ser referenciadas somente dentro do procedimento em que foram definidas.</span><span class="sxs-lookup"><span data-stu-id="6fc9f-404">For example, local variables can be referenced only within the procedure in which they were defined.</span></span> <span data-ttu-id="6fc9f-405">As variáveis públicas podem ser acessadas de qualquer lugar no aplicativo.</span><span class="sxs-lookup"><span data-stu-id="6fc9f-405">Public variables are accessible from anywhere in the application.</span></span> <span data-ttu-id="6fc9f-406">Objetos, como o banco de dados atual, estão no escopo se eles estão no caminho de pesquisa definido.</span><span class="sxs-lookup"><span data-stu-id="6fc9f-406">Objects, such as the current database, are in scope if they are in the defined search path.</span></span> <span data-ttu-id="6fc9f-407">Os intervalos de registros podem ser especificados com uma cláusula Scope em muitos comandos.</span><span class="sxs-lookup"><span data-stu-id="6fc9f-407">Record ranges can be specified with a Scope clause in many commands.</span></span>

<span data-ttu-id="6fc9f-408">**provedor de serviços**</span><span class="sxs-lookup"><span data-stu-id="6fc9f-408">**service provider**</span></span>

<span data-ttu-id="6fc9f-409">Software que encapsula um serviço produzindo e consumindo dados, aumentando os recursos em seus aplicativos ADO.</span><span class="sxs-lookup"><span data-stu-id="6fc9f-409">Software that encapsulates a service by producing and consuming data, augmenting features in your ADO applications.</span></span> <span data-ttu-id="6fc9f-410">É um provedor que não expõe dados diretamente, em vez disso, fornece um serviço, como o processamento de consultas.</span><span class="sxs-lookup"><span data-stu-id="6fc9f-410">It is a provider that does not directly expose data, rather it provides a service, such as query processing.</span></span> <span data-ttu-id="6fc9f-411">O provedor de serviços pode processar dados fornecidos por um provedor de dados.</span><span class="sxs-lookup"><span data-stu-id="6fc9f-411">The service provider may process data provided by a data provider.</span></span> <span data-ttu-id="6fc9f-412">Consulte também o **provedor de dados.**</span><span class="sxs-lookup"><span data-stu-id="6fc9f-412">See also **data provider**.</span></span>

<span data-ttu-id="6fc9f-413">**Recordset com formato**</span><span class="sxs-lookup"><span data-stu-id="6fc9f-413">**shaped Recordset**</span></span>

<span data-ttu-id="6fc9f-414">Um **Recordset** cujas colunas foram especificamente definidas para conter não apenas dados, mas também referências (chamadas de capítulos) a outros objetos **Recordset** e/ou valores calculados com base em outros objetos **Recordset.**</span><span class="sxs-lookup"><span data-stu-id="6fc9f-414">A **Recordset** whose columns have been specifically defined to contain not just data, but also references (called chapters) to other **Recordset** objects and/or computed values based on other **Recordset** objects.</span></span>

<span data-ttu-id="6fc9f-415">**sibling**</span><span class="sxs-lookup"><span data-stu-id="6fc9f-415">**sibling**</span></span>

<span data-ttu-id="6fc9f-416">Qualquer dois ou mais nós em uma estrutura hierárquica que estão no mesmo nível na hierarquia.</span><span class="sxs-lookup"><span data-stu-id="6fc9f-416">Any two or more nodes in a hierarchical structure that are on the same level in the hierarchy.</span></span> <span data-ttu-id="6fc9f-417">O nó raiz em uma hierarquia não tem irmãos.</span><span class="sxs-lookup"><span data-stu-id="6fc9f-417">The root node in a hierarchy has no siblings.</span></span>

<span data-ttu-id="6fc9f-418">**procedimento armazenado**</span><span class="sxs-lookup"><span data-stu-id="6fc9f-418">**stored procedure**</span></span>

<span data-ttu-id="6fc9f-419">Uma coleção pré-compilada de código, como instruções SQL e instruções opcionais de controle de fluxo armazenadas em um nome e processadas como uma unidade.</span><span class="sxs-lookup"><span data-stu-id="6fc9f-419">A precompiled collection of code such as SQL statements and optional control-of-flow statements stored under a name and processed as a unit.</span></span> <span data-ttu-id="6fc9f-420">Os procedimentos armazenados são armazenados em um banco de dados; eles podem ser executados com uma chamada de um aplicativo e permitir variáveis declaradas pelo usuário, execução condicional e outros recursos avançados de programação.</span><span class="sxs-lookup"><span data-stu-id="6fc9f-420">Stored procedures are stored within a database; they can be executed with one call from an application and allow user-declared variables, conditional execution, and other powerful programming features.</span></span>

<span data-ttu-id="6fc9f-421">**stub**</span><span class="sxs-lookup"><span data-stu-id="6fc9f-421">**stub**</span></span>

<span data-ttu-id="6fc9f-422">Um objeto específico da interface que fornece o empacotamento do parâmetro e a comunicação necessária para que um objeto de aplicativo receba chamadas de um cliente que está sendo executado em um ambiente de execução diferente, como em um thread diferente ou em outro processo.</span><span class="sxs-lookup"><span data-stu-id="6fc9f-422">An interface-specific object that provides the parameter marshaling and communication required for an application object to receive calls from a client that is running in a different execution environment, such as on a different thread or in another process.</span></span> <span data-ttu-id="6fc9f-423">O stub está localizado com o objeto application e se comunica com um proxy correspondente que está localizado com o cliente que o chama.</span><span class="sxs-lookup"><span data-stu-id="6fc9f-423">The stub is located with the application object and communicates with a corresponding proxy that is located with the client that calls it.</span></span> <span data-ttu-id="6fc9f-424">Consulte também **proxy**.</span><span class="sxs-lookup"><span data-stu-id="6fc9f-424">See also **proxy**.</span></span>

<span data-ttu-id="6fc9f-425">**sub-nó**</span><span class="sxs-lookup"><span data-stu-id="6fc9f-425">**sub-node**</span></span>

<span data-ttu-id="6fc9f-426">Ver **filho**.</span><span class="sxs-lookup"><span data-stu-id="6fc9f-426">See **child**.</span></span>

<span data-ttu-id="6fc9f-427">**operação síncrona**</span><span class="sxs-lookup"><span data-stu-id="6fc9f-427">**synchronous operation**</span></span>

<span data-ttu-id="6fc9f-428">Uma operação iniciada pelo código que é concluída antes do início da próxima operação.</span><span class="sxs-lookup"><span data-stu-id="6fc9f-428">An operation initiated by code that completes before the next operation may start.</span></span> <span data-ttu-id="6fc9f-429">Consulte também **a operação assíncrona.**</span><span class="sxs-lookup"><span data-stu-id="6fc9f-429">See also **asynchronous operation**.</span></span>

<span data-ttu-id="6fc9f-430">Retornar ao início</span><span class="sxs-lookup"><span data-stu-id="6fc9f-430">Return to top</span></span>

## <a name="t-w"></a><span data-ttu-id="6fc9f-431">T-W</span><span class="sxs-lookup"><span data-stu-id="6fc9f-431">T-W</span></span>

<span data-ttu-id="6fc9f-432">**árvore**</span><span class="sxs-lookup"><span data-stu-id="6fc9f-432">**tree**</span></span>

<span data-ttu-id="6fc9f-433">Uma estrutura que representa uma relação hierárquica entre elementos (nós).</span><span class="sxs-lookup"><span data-stu-id="6fc9f-433">A structure representing a hierarchical relationship between elements (nodes).</span></span> <span data-ttu-id="6fc9f-434">Há um nó no nível superior de uma árvore (a raiz).</span><span class="sxs-lookup"><span data-stu-id="6fc9f-434">There is one node at the top level of a tree (the root).</span></span> <span data-ttu-id="6fc9f-435">Sob a raiz, pode haver vários filhos.</span><span class="sxs-lookup"><span data-stu-id="6fc9f-435">Underneath the root, there can be multiple children.</span></span> <span data-ttu-id="6fc9f-436">Cada filho, por sua vez, pode ser pai de outros filhos, ramificando assim como uma árvore.</span><span class="sxs-lookup"><span data-stu-id="6fc9f-436">Each child may in turn be the parent of other children, thus branching like a tree.</span></span> <span data-ttu-id="6fc9f-437">Uma pasta que contém documentos e outras pastas é um exemplo típico de uma estrutura de árvore.</span><span class="sxs-lookup"><span data-stu-id="6fc9f-437">A folder containing documents and other folders is a typical example of a tree structure.</span></span> <span data-ttu-id="6fc9f-438">See also **hierarchy**, **node**, **root**, **child**, **parent**.</span><span class="sxs-lookup"><span data-stu-id="6fc9f-438">See also **hierarchy**, **node**, **root**, **child**, **parent**.</span></span>

<span data-ttu-id="6fc9f-439">**URL (Uniform Resource Locator)**</span><span class="sxs-lookup"><span data-stu-id="6fc9f-439">**URL (Uniform Resource Locator)**</span></span>

<span data-ttu-id="6fc9f-440">Especifica a localização de um recurso que reside na Internet ou em uma intranet.</span><span class="sxs-lookup"><span data-stu-id="6fc9f-440">Specifies the location of a resource residing on the Internet or an intranet.</span></span> <span data-ttu-id="6fc9f-441">Uma URL completa consiste em um esquema (como FTP, HTTP, mailto, arquivo e assim por diante), seguido por dois pontos, um nome de servidor e o caminho completo de um recurso (como um documento, gráfico ou outro arquivo).</span><span class="sxs-lookup"><span data-stu-id="6fc9f-441">A complete URL consists of a scheme (such as FTP, HTTP, mailto, file, and so on), followed by a colon, a server name, and the full path of a resource (such as a document, graphic, or other file).</span></span> <span data-ttu-id="6fc9f-442">Alguns exemplos de URLs são:</span><span class="sxs-lookup"><span data-stu-id="6fc9f-442">Some examples of URLs are:</span></span>  
  
- https://www.domain.com/default.html  
- <span data-ttu-id="6fc9f-443">ftp://ftp.server.somewhere/ftp.file</span><span class="sxs-lookup"><span data-stu-id="6fc9f-443">ftp://ftp.server.somewhere/ftp.file</span></span>  
  
- <span data-ttu-id="6fc9f-444">ftp://ftp.server.somewhere/ftp.file</span><span class="sxs-lookup"><span data-stu-id="6fc9f-444">ftp://ftp.server.somewhere/ftp.file</span></span>  
- <span data-ttu-id="6fc9f-445">file://Server/Share/File.doc</span><span class="sxs-lookup"><span data-stu-id="6fc9f-445">file://Server/Share/File.doc</span></span>

<span data-ttu-id="6fc9f-446">Consulte também **a URL absoluta** e a URL **relativa.**</span><span class="sxs-lookup"><span data-stu-id="6fc9f-446">See also **absolute URL** and **relative URL**.</span></span>

<span data-ttu-id="6fc9f-447">**servidor Web**</span><span class="sxs-lookup"><span data-stu-id="6fc9f-447">**web server**</span></span>

<span data-ttu-id="6fc9f-448">Um computador que fornece serviços Web e páginas para usuários da intranet e da Internet.</span><span class="sxs-lookup"><span data-stu-id="6fc9f-448">A computer that provides web services and pages to intranet and Internet users.</span></span>



