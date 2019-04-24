---
title: Usando as extensões do Visual C++
TOCTitle: Using Visual C++ Extensions
ms:assetid: 0fb1014c-7ab6-6add-d09f-e5e48b2b32cb
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248866(v=office.15)
ms:contentKeyID: 48543270
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 8bf2234e5935c2a1a13871e7e45c980fb9f33109
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32312058"
---
# <a name="using-visual-c-extensions"></a><span data-ttu-id="5f0fe-102">Uso de Extensões do Visual C++</span><span class="sxs-lookup"><span data-stu-id="5f0fe-102">Using Visual C++ Extensions</span></span>


<span data-ttu-id="5f0fe-103">**Aplica-se ao:** Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="5f0fe-103">**Applies to**: Access 2013, Office 2013</span></span>

## <a name="the-iadorecordbinding-interface"></a><span data-ttu-id="5f0fe-104">A interface IADORecordBinding</span><span class="sxs-lookup"><span data-stu-id="5f0fe-104">The IADORecordBinding Interface</span></span>

<span data-ttu-id="5f0fe-p101">As extensões do Microsoft Visual C++ para ADO associam, ou acoplam, os campos de um objeto [Recordset](recordset-object-ado.md) às variáveis C/C++. Sempre que a linha atual do **Recordset** acoplado é alterada, todos os campos acoplados no **Recordset** são copiados para essas variáveis. Se necessário, os dados copiados são convertidos no tipo de dados declarado da variável C/C++.</span><span class="sxs-lookup"><span data-stu-id="5f0fe-p101">The Microsoft Visual C++ Extensions for ADO associate, or bind, fields of a [Recordset](recordset-object-ado.md) object to C/C++ variables. Whenever the current row of the bound **Recordset** changes, all the bound fields in the **Recordset** are copied to the C/C++ variables. If necessary, the copied data is converted to the declared data type of the C/C++ variable.</span></span>

<span data-ttu-id="5f0fe-p102">O método **BindToRecordset** da interface **IADORecordBinding** acopla campos às variáveis C/C++. O método **AddNew** adiciona uma nova linha ao **Recordset** acoplado. O método **Update** preenche os campos nas novas linhas de **Recordset** ou atualiza os campos nas linhas existentes, com o valor das variáveis C/C++.</span><span class="sxs-lookup"><span data-stu-id="5f0fe-p102">The **BindToRecordset** method of the **IADORecordBinding** interface binds fields to C/C++ variables. The **AddNew** method adds a new row to the bound **Recordset**. The **Update** method populates fields in new rows of the **Recordset**, or updates fields in existing rows, with the value of the C/C++ variables.</span></span>

<span data-ttu-id="5f0fe-p103">A interface **IADORecordBinding** é implementada pelo objeto **Recordset**. Não é possível codificar a implementação sozinho.</span><span class="sxs-lookup"><span data-stu-id="5f0fe-p103">The **IADORecordBinding** interface is implemented by the **Recordset** object. You do not code the implementation yourself.</span></span>

## <a name="binding-entries"></a><span data-ttu-id="5f0fe-113">Entradas de ligação</span><span class="sxs-lookup"><span data-stu-id="5f0fe-113">Binding Entries</span></span>

<span data-ttu-id="5f0fe-p104">As extensões do Visual C++ para ADO mapeiam os campos de um objeto [Recordset](recordset-object-ado.md) para as variáveis C/C++. A definição de um mapeamento entre um campo e uma variável é chamada *entrada de ligação*. As macros fornecem entradas de ligação para dados numéricos de tamanhos fixo e variável. As entradas de ligação e as variáveis C/C++ são declaradas em uma classe derivada da classe **CADORecordBinding** de extensões do Visual C++. A classe **CADORecordBinding** é definida internamente pelas macros de entrada de ligação.</span><span class="sxs-lookup"><span data-stu-id="5f0fe-p104">The Visual C++ Extensions for ADO map fields of a [Recordset](recordset-object-ado.md) object to C/C++ variables. The definition of a mapping between a field and a variable is called a *binding entry*. Macros provide binding entries for numeric, fixed-length, and variable-length data. The binding entries and C/C++ variables are declared in a class derived from the Visual C++ Extensions class, **CADORecordBinding**. The **CADORecordBinding** class is defined internally by the binding entry macros.</span></span>

<span data-ttu-id="5f0fe-p105">O ADO mapeia internamente os parâmetros nessas macros para uma estrutura **DBBINDING** do OLE DB e cria um objeto **Accessor** do OLE DB para gerenciar o movimento e a conversão de dados entre campos e variáveis. O OLE DB define os dados em três partes: um *buffer* para repositório dos dados; um *status* que indica se um campo foi armazenado com êxito no buffer, ou como a variável deve ser restaurada para o campo; e o *comprimento* dos dados. (Para obter mais informações, consulte *OLE DB Programmer's Reference*, capítulo 6: Getting and Setting Data [em inglês].)</span><span class="sxs-lookup"><span data-stu-id="5f0fe-p105">ADO internally maps the parameters in these macros to an OLE DB **DBBINDING** structure and creates an OLE DB **Accessor** object to manage the movement and conversion of data between fields and variables. OLE DB defines data as consisting of three parts: A *buffer* where the data is stored; a *status* that indicates whether a field was successfully stored in the buffer, or how the variable should be restored to the field; and the *length* of the data. (See the *OLE DB Programmer's Reference*, Chapter 6: Getting and Setting Data for more information.)</span></span>

## <a name="header-file"></a><span data-ttu-id="5f0fe-122">Arquivo de cabeçalho</span><span class="sxs-lookup"><span data-stu-id="5f0fe-122">Header File</span></span>

<span data-ttu-id="5f0fe-123">Inclua o arquivo a seguir em seu aplicativo para usar as extensões do Visual C++ para ADO:</span><span class="sxs-lookup"><span data-stu-id="5f0fe-123">Include the following file in your application in order to use the Visual C++ Extensions for ADO:</span></span>

```cpp 
 
#include <icrsint.h> 
```

## <a name="binding-recordset-fields"></a><span data-ttu-id="5f0fe-124">Acoplando campos de Recordset</span><span class="sxs-lookup"><span data-stu-id="5f0fe-124">Binding Recordset Fields</span></span>

<span data-ttu-id="5f0fe-125">**Para acoplar campos de Recordset às variáveis C/C++**</span><span class="sxs-lookup"><span data-stu-id="5f0fe-125">**To Bind Recordset Fields to C/C++ Variables**</span></span>

1.  <span data-ttu-id="5f0fe-126">Crie uma classe derivada da classe **CADORecordBinding**.</span><span class="sxs-lookup"><span data-stu-id="5f0fe-126">Create a class derived from the **CADORecordBinding** class.</span></span>

2.  <span data-ttu-id="5f0fe-127">Especifique as entradas de ligação e as variáveis C/C++ correspondentes na classe derivada.</span><span class="sxs-lookup"><span data-stu-id="5f0fe-127">Specify binding entries and corresponding C/C++ variables in the derived class.</span></span> <span data-ttu-id="5f0fe-128">Colchete as entradas de associação **entre\_Begin\_Binding ADO** e **\_end\_ADO Binding** macros.</span><span class="sxs-lookup"><span data-stu-id="5f0fe-128">Bracket the binding entries between **BEGIN\_ADO\_BINDING** and **END\_ADO\_BINDING** macros.</span></span> <span data-ttu-id="5f0fe-129">Não termine as macros com vírgula ou ponto-e-vírgula.</span><span class="sxs-lookup"><span data-stu-id="5f0fe-129">Do not terminate the macros with commas or semicolons.</span></span> <span data-ttu-id="5f0fe-130">Delimitadores apropriados são especificados automaticamente por cada macro.</span><span class="sxs-lookup"><span data-stu-id="5f0fe-130">Appropriate delimiters are specified automatically by each macro.</span></span> <span data-ttu-id="5f0fe-131">Especifique uma entrada de ligação para cada campo a ser mapeado para uma variável C/C++.</span><span class="sxs-lookup"><span data-stu-id="5f0fe-131">Specify one binding entry for each field to be mapped to a C/C++ variable.</span></span> <span data-ttu-id="5f0fe-132">Use um membro apropriado da **entrada de\_tamanho\_\_fixo do ADO**, da **entrada\_numérica\_do ADO**ou da família de entrada de **tamanho\_\_\_variável do ADO** .</span><span class="sxs-lookup"><span data-stu-id="5f0fe-132">Use an appropriate member from the **ADO\_FIXED\_LENGTH\_ENTRY**, **ADO\_NUMERIC\_ENTRY**, or **ADO\_VARIABLE\_LENGTH\_ENTRY** family of macros.</span></span>

3.  <span data-ttu-id="5f0fe-p107">No seu aplicativo, crie uma instância da classe derivada de **CADORecordBinding**. Obtenha a interface **IADORecordBinding** de **Recordset**. Em seguida, chame o método **BindToRecordset** para acoplar os campos **Recordset** às variáveis C/C++.</span><span class="sxs-lookup"><span data-stu-id="5f0fe-p107">In your application, create an instance of the class derived from **CADORecordBinding**. Get the **IADORecordBinding** interface from the **Recordset**. Then call the **BindToRecordset** method to bind the **Recordset** fields to the C/C++ variables.</span></span>

<span data-ttu-id="5f0fe-136">Consulte o [Exemplo de extensões do Visual C++](visual-c-extensions-example.md) para obter mais informações.</span><span class="sxs-lookup"><span data-stu-id="5f0fe-136">See the [Visual C++ Extensions Example](visual-c-extensions-example.md) for more information.</span></span>

## <a name="interface-methods"></a><span data-ttu-id="5f0fe-137">Métodos de interface</span><span class="sxs-lookup"><span data-stu-id="5f0fe-137">Interface Methods</span></span>

<span data-ttu-id="5f0fe-p108">A interface **IADORecordBinding** possui três métodos: **BindToRecordset**, **AddNew** e **Update**. O único argumento de cada método é um ponteiro para uma instância da classe derivada de **CADORecordBinding**. Portanto, os métodos **AddNew** e **Update** não podem especificar nenhum parâmetro de seus homônimos de método ADO.</span><span class="sxs-lookup"><span data-stu-id="5f0fe-p108">The **IADORecordBinding** interface has three methods: **BindToRecordset**, **AddNew**, and **Update**. The sole argument to each method is a pointer to an instance of the class derived from **CADORecordBinding**. Therefore, the **AddNew** and **Update** methods cannot specify any of the parameters of their ADO method namesakes.</span></span>

<span data-ttu-id="5f0fe-141">**Sintaxe**</span><span class="sxs-lookup"><span data-stu-id="5f0fe-141">**Syntax**</span></span>

<span data-ttu-id="5f0fe-142">O método **BindToRecordset** associa os campos **Recordset** às variáveis C/C++.</span><span class="sxs-lookup"><span data-stu-id="5f0fe-142">The **BindToRecordset** method associates the **Recordset** fields with C/C++ variables.</span></span>

`BindToRecordset(CADORecordBinding *binding)` 

<span data-ttu-id="5f0fe-143">O método **AddNew** chama seu homônimo, o método ADO [AddNew](addnew-method-ado.md), para adicionar uma nova linha a **Recordset**.</span><span class="sxs-lookup"><span data-stu-id="5f0fe-143">The **AddNew** method invokes its namesake, the ADO [AddNew](addnew-method-ado.md) method, to add a new row to the **Recordset**.</span></span>

`AddNew(CADORecordBinding *binding)` 

<span data-ttu-id="5f0fe-144">O método **Update** chama seu homônimo, o método ADO [Update](update-method-ado.md), para atualizar o **Recordset**.</span><span class="sxs-lookup"><span data-stu-id="5f0fe-144">The **Update** method invokes its namesake, the ADO [Update](update-method-ado.md) method, to update the **Recordset**.</span></span>

`Update(CADORecordBinding *binding)` 

## <a name="binding-entry-macros"></a><span data-ttu-id="5f0fe-145">Macros de entrada de ligação</span><span class="sxs-lookup"><span data-stu-id="5f0fe-145">Binding Entry Macros</span></span>

<span data-ttu-id="5f0fe-p109">As macros de entrada de ligação definem a associação de um campo **Recordset** e uma variável. Uma macro inicial e uma macro final delimitam o conjunto de entradas de ligação.</span><span class="sxs-lookup"><span data-stu-id="5f0fe-p109">Binding entry macros define the association of a **Recordset** field and a variable. A beginning and ending macro delimits the set of binding entries.</span></span>

<span data-ttu-id="5f0fe-p110">As famílias de macros são fornecidas para dados de comprimento fixo, como **adDate** ou **adBoolean**; dados numéricos, como **adTinyInt**, **adInteger** ou **adDouble**; e dados de comprimento variável, como **adChar**, **adVarChar** ou **adVarBinary**. Todos os tipos numéricos, exceto **adVarNumeric**, também são tipos de comprimento fixo. Cada família possui conjuntos de parâmetros diferentes, o que permite excluir as informações de ligação que não sejam de seu interesse.</span><span class="sxs-lookup"><span data-stu-id="5f0fe-p110">Families of macros are provided for fixed-length data, such as **adDate** or **adBoolean**; numeric data, such as **adTinyInt**, **adInteger**, or **adDouble**; and variable-length data, such as **adChar**, **adVarChar** or **adVarBinary**. All numeric types, except for **adVarNumeric**, are also fixed-length types. Each family has differing sets of parameters so that you can exclude binding information that is of no interest.</span></span>

<span data-ttu-id="5f0fe-151">Para obter informações adicionais, consulte a *Referência do programador do OLE DB*, apêndice A: Tipos de dados.</span><span class="sxs-lookup"><span data-stu-id="5f0fe-151">See the *OLE DB Programmer's Reference,* Appendix A: Data Types for additional information.</span></span>

<span data-ttu-id="5f0fe-152">_**Início das entradas de ligação**_</span><span class="sxs-lookup"><span data-stu-id="5f0fe-152">_**Begin Binding Entries**_</span></span>

<span data-ttu-id="5f0fe-153">**INICIAR\_Associação\_ADO**(*classe*)</span><span class="sxs-lookup"><span data-stu-id="5f0fe-153">**BEGIN\_ADO\_BINDING**(*Class*)</span></span>

<span data-ttu-id="5f0fe-154">_**Dados de comprimento fixo**_</span><span class="sxs-lookup"><span data-stu-id="5f0fe-154">_**Fixed-Length Data**_</span></span>

<span data-ttu-id="5f0fe-155">**Entrada\_de\_tamanho\_fixo ADO**(*ordinal, DataType, buffer, status, modificar*)</span><span class="sxs-lookup"><span data-stu-id="5f0fe-155">**ADO\_FIXED\_LENGTH\_ENTRY**(*Ordinal, DataType, Buffer, Status, Modify*)</span></span>  
<span data-ttu-id="5f0fe-156">**Tamanho\_fixo\_do ADO\_ENTRY2**(*ordinal, DataType, buffer, Modify*)</span><span class="sxs-lookup"><span data-stu-id="5f0fe-156">**ADO\_FIXED\_LENGTH\_ENTRY2**(*Ordinal, DataType, Buffer, Modify*)</span></span>

<span data-ttu-id="5f0fe-157">_**Dados numéricos**_</span><span class="sxs-lookup"><span data-stu-id="5f0fe-157">_**Numeric Data**_</span></span>

<span data-ttu-id="5f0fe-158">**Entrada\_numérica\_do ADO**(*ordinal, DataType, buffer, precisão, escala, status, modificar*)</span><span class="sxs-lookup"><span data-stu-id="5f0fe-158">**ADO\_NUMERIC\_ENTRY**(*Ordinal, DataType, Buffer, Precision, Scale, Status, Modify*)</span></span>  
<span data-ttu-id="5f0fe-159">**ADO\_numérico\_ENTRY2**(*ordinal, DataType, buffer, precisão, escala, modificar*)</span><span class="sxs-lookup"><span data-stu-id="5f0fe-159">**ADO\_NUMERIC\_ENTRY2**(*Ordinal, DataType, Buffer, Precision, Scale, Modify*)</span></span>

<span data-ttu-id="5f0fe-160">_**Dados de comprimento variável**_</span><span class="sxs-lookup"><span data-stu-id="5f0fe-160">_**Variable-Length Data**_</span></span>

<span data-ttu-id="5f0fe-161">**Entrada\_de\_tamanho\_da variável ADO**(*ordinal, DataType, buffer, tamanho, status, comprimento, modificar*)</span><span class="sxs-lookup"><span data-stu-id="5f0fe-161">**ADO\_VARIABLE\_LENGTH\_ENTRY**(*Ordinal, DataType, Buffer, Size, Status, Length, Modify*)</span></span>  
<span data-ttu-id="5f0fe-162">**Comprimento\_variável\_ADO\_ENTRY2**(*ordinal, DataType, buffer, tamanho, status, modificar*)</span><span class="sxs-lookup"><span data-stu-id="5f0fe-162">**ADO\_VARIABLE\_LENGTH\_ENTRY2**(*Ordinal, DataType, Buffer, Size, Status, Modify*)</span></span>  
<span data-ttu-id="5f0fe-163">**Comprimento\_variável\_ADO\_ENTRY3**(*ordinal, DataType, buffer, tamanho, comprimento, modificar*)</span><span class="sxs-lookup"><span data-stu-id="5f0fe-163">**ADO\_VARIABLE\_LENGTH\_ENTRY3**(*Ordinal, DataType, Buffer, Size, Length, Modify*)</span></span>  
<span data-ttu-id="5f0fe-164">**Comprimento\_variável\_ADO\_ENTRY4**(*ordinal, DataType, buffer, tamanho, modificar*)</span><span class="sxs-lookup"><span data-stu-id="5f0fe-164">**ADO\_VARIABLE\_LENGTH\_ENTRY4**(*Ordinal, DataType, Buffer, Size, Modify*)</span></span>

<span data-ttu-id="5f0fe-165">_**Encerrar entradas de vinculação**_</span><span class="sxs-lookup"><span data-stu-id="5f0fe-165">_**End Binding Entries**_</span></span>

<span data-ttu-id="5f0fe-166">**Encerrar\_Associação\_ADO** ()</span><span class="sxs-lookup"><span data-stu-id="5f0fe-166">**END\_ADO\_BINDING**()</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="5f0fe-167">Parâmetro</span><span class="sxs-lookup"><span data-stu-id="5f0fe-167">Parameter</span></span></p></th>
<th><p><span data-ttu-id="5f0fe-168">Descrição</span><span class="sxs-lookup"><span data-stu-id="5f0fe-168">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="5f0fe-169"><em>Classe</em></span><span class="sxs-lookup"><span data-stu-id="5f0fe-169"><em>Class</em></span></span></p></td>
<td><p><span data-ttu-id="5f0fe-170">Classe na qual são definidas as entradas de ligação e as variáveis C/C++.</span><span class="sxs-lookup"><span data-stu-id="5f0fe-170">Class in which the binding entries and C/C++ variables are defined.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5f0fe-171"><em>Ordinal</em></span><span class="sxs-lookup"><span data-stu-id="5f0fe-171"><em>Ordinal</em></span></span></p></td>
<td><p><span data-ttu-id="5f0fe-172">Número ordinal, contado a partir de um, do campo <strong>Recordset</strong> correspondente a sua variável C/C++.</span><span class="sxs-lookup"><span data-stu-id="5f0fe-172">Ordinal number, counting from one, of the <strong>Recordset</strong> field corresponding to your C/C++ variable.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5f0fe-173"><em>DataType</em></span><span class="sxs-lookup"><span data-stu-id="5f0fe-173"><em>DataType</em></span></span></p></td>
<td><p><span data-ttu-id="5f0fe-p111">Tipo de dados ADO equivalente da variável C/C++ (consulte <a href="datatypeenum.md">DataTypeEnum</a> para obter uma lista de tipos de dados válidos). Se necessário, o valor do campo <strong>Recordset</strong> será convertido nesse tipo de dados.</span><span class="sxs-lookup"><span data-stu-id="5f0fe-p111">Equivalent ADO data type of the C/C++ variable (see <a href="datatypeenum.md">DataTypeEnum</a> for a list of valid data types). The value of the <strong>Recordset</strong> field will be converted to this data type if necessary.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5f0fe-176"><em>Buffer</em></span><span class="sxs-lookup"><span data-stu-id="5f0fe-176"><em>Buffer</em></span></span></p></td>
<td><p><span data-ttu-id="5f0fe-177">Nome da variável C/C++ de repositório do campo <strong>Recordset</strong>.</span><span class="sxs-lookup"><span data-stu-id="5f0fe-177">Name of the C/C++ variable where the <strong>Recordset</strong> field will be stored.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5f0fe-178"><em>Tamanho</em></span><span class="sxs-lookup"><span data-stu-id="5f0fe-178"><em>Size</em></span></span></p></td>
<td><p><span data-ttu-id="5f0fe-179">Tamanho máximo, em bytes, de <em>Buffer</em>.</span><span class="sxs-lookup"><span data-stu-id="5f0fe-179">Maximum size in bytes of <em>Buffer</em>.</span></span> <span data-ttu-id="5f0fe-180">Se <em>Buffer</em> contiver uma sequência de caracteres de comprimento variável, deixe espaço para um zero de terminação.</span><span class="sxs-lookup"><span data-stu-id="5f0fe-180">If <em>Buffer</em> will contain a variable-length string, allow room for a terminating zero.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5f0fe-181"><em>Status</em></span><span class="sxs-lookup"><span data-stu-id="5f0fe-181"><em>Status</em></span></span></p></td>
<td><p><span data-ttu-id="5f0fe-182">Nome de uma variável que indicará se o conteúdo de <em>Buffer</em> é válido e se a conversão do campo em <em>DataType</em> foi bem-sucedida.</span><span class="sxs-lookup"><span data-stu-id="5f0fe-182">Name of a variable that will indicate whether the contents of <em>Buffer</em> are valid, and whether the conversion of the field to <em>DataType</em> was successful.</span></span> <span data-ttu-id="5f0fe-183">Os dois valores mais importantes dessa variável são <strong>adFldOK</strong>, indicando que a conversão foi bem-sucedida; e <strong>adFldNull</strong>, indicando que o valor do campo será um VARIANT de tipo VT_NULL, e não simplesmente vazio.</span><span class="sxs-lookup"><span data-stu-id="5f0fe-183">The two most important values for this variable are <strong>adFldOK</strong>, which means the conversion was successful; and <strong>adFldNull</strong>, which means the value of the field would be a VARIANT of type VT_NULL and not merely empty.</span></span> <span data-ttu-id="5f0fe-184">Os valores possíveis para <em>status</em> estão listados na próxima tabela, &quot;valores de status.&quot;</span><span class="sxs-lookup"><span data-stu-id="5f0fe-184">Possible values for <em>Status</em> are listed in the next table, &quot;Status Values.&quot;</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5f0fe-185"><em>Modificar</em></span><span class="sxs-lookup"><span data-stu-id="5f0fe-185"><em>Modify</em></span></span></p></td>
<td><p><span data-ttu-id="5f0fe-186">Sinalizador booleano; se for TRUE, indicará que o ADO tem permissão para atualizar o campo <strong>Recordset</strong> correspondente com o valor contido em <em>Buffer</em>.</span><span class="sxs-lookup"><span data-stu-id="5f0fe-186">Boolean flag; if TRUE, indicates ADO is allowed to update the corresponding <strong>Recordset</strong> field with the value contained in <em>Buffer</em>.</span></span> <span data-ttu-id="5f0fe-187">Defina o parâmetro booleano <em>modify</em> como TRUE para permitir que o ADO atualize o campo acoplado e como FALSE se desejar examinar o campo, mas sem alterá-lo.</span><span class="sxs-lookup"><span data-stu-id="5f0fe-187">Set the Boolean <em>modify</em> parameter to TRUE to enable ADO to update the bound field, and FALSE if you want to examine the field but not change it.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5f0fe-188"><em>Precisão</em></span><span class="sxs-lookup"><span data-stu-id="5f0fe-188"><em>Precision</em></span></span></p></td>
<td><p><span data-ttu-id="5f0fe-189">Número de dígitos que podem ser representados em uma variável numérica.</span><span class="sxs-lookup"><span data-stu-id="5f0fe-189">Number of digits that can be represented in a numeric variable.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5f0fe-190"><em>Escala</em></span><span class="sxs-lookup"><span data-stu-id="5f0fe-190"><em>Scale</em></span></span></p></td>
<td><p><span data-ttu-id="5f0fe-191">Número de casas decimais em uma variável numérica.</span><span class="sxs-lookup"><span data-stu-id="5f0fe-191">Number of decimal places in a numeric variable.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5f0fe-192"><em>Length</em></span><span class="sxs-lookup"><span data-stu-id="5f0fe-192"><em>Length</em></span></span></p></td>
<td><p><span data-ttu-id="5f0fe-193">Nome de uma variável de quatro bytes que conterá o comprimento real dos dados em <em>Buffer</em>.</span><span class="sxs-lookup"><span data-stu-id="5f0fe-193">Name of a four-byte variable that will contain the actual length of the data in <em>Buffer</em>.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="status-values"></a><span data-ttu-id="5f0fe-194">Valores de status</span><span class="sxs-lookup"><span data-stu-id="5f0fe-194">Status Values</span></span>

<span data-ttu-id="5f0fe-195">O valor da variável *Status* indica se um campo foi copiado com êxito para uma variável.</span><span class="sxs-lookup"><span data-stu-id="5f0fe-195">The value of the *Status* variable indicates whether a field was successfully copied to a variable.</span></span>

<span data-ttu-id="5f0fe-196">Ao configurar os dados, defina *Status* como **adFldNull** para indicar que o campo **Recordset** seja definido como nulo.</span><span class="sxs-lookup"><span data-stu-id="5f0fe-196">When setting data, *Status* may be set to **adFldNull** to indicate the **Recordset** field should be set to null.</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="5f0fe-197">Constant</span><span class="sxs-lookup"><span data-stu-id="5f0fe-197">Constant</span></span></p></th>
<th><p><span data-ttu-id="5f0fe-198">Valor</span><span class="sxs-lookup"><span data-stu-id="5f0fe-198">Value</span></span></p></th>
<th><p><span data-ttu-id="5f0fe-199">Descrição</span><span class="sxs-lookup"><span data-stu-id="5f0fe-199">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="5f0fe-200"><strong>adFldOK</strong></span><span class="sxs-lookup"><span data-stu-id="5f0fe-200"><strong>adFldOK</strong></span></span></p></td>
<td><p><span data-ttu-id="5f0fe-201">,0</span><span class="sxs-lookup"><span data-stu-id="5f0fe-201">0</span></span></p></td>
<td><p><span data-ttu-id="5f0fe-202">Um valor de campo não-nulo foi retornado.</span><span class="sxs-lookup"><span data-stu-id="5f0fe-202">A non-null field value was returned.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5f0fe-203"><strong>adFldBadAccessor</strong></span><span class="sxs-lookup"><span data-stu-id="5f0fe-203"><strong>adFldBadAccessor</strong></span></span></p></td>
<td><p><span data-ttu-id="5f0fe-204">1</span><span class="sxs-lookup"><span data-stu-id="5f0fe-204">1</span></span></p></td>
<td><p><span data-ttu-id="5f0fe-205">A ligação era inválida.</span><span class="sxs-lookup"><span data-stu-id="5f0fe-205">Binding was invalid.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5f0fe-206"><strong>adFldCantConvertValue</strong></span><span class="sxs-lookup"><span data-stu-id="5f0fe-206"><strong>adFldCantConvertValue</strong></span></span></p></td>
<td><p><span data-ttu-id="5f0fe-207">duas</span><span class="sxs-lookup"><span data-stu-id="5f0fe-207">2</span></span></p></td>
<td><p><span data-ttu-id="5f0fe-208">O valor não pôde ser convertido devido a razões diferentes de incompatibilidade de sinal ou estouro de dados.</span><span class="sxs-lookup"><span data-stu-id="5f0fe-208">Value couldn't be converted for reasons other than sign mismatch or data overflow.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5f0fe-209"><strong>adFldNull</strong></span><span class="sxs-lookup"><span data-stu-id="5f0fe-209"><strong>adFldNull</strong></span></span></p></td>
<td><p><span data-ttu-id="5f0fe-210">3D</span><span class="sxs-lookup"><span data-stu-id="5f0fe-210">3</span></span></p></td>
<td><p><span data-ttu-id="5f0fe-211">Quando um campo é obtido, indica que um valor nulo foi retornado.</span><span class="sxs-lookup"><span data-stu-id="5f0fe-211">When getting a field, indicates a null value was returned.</span></span> <span data-ttu-id="5f0fe-212">Na configuração de um campo, indica que o campo deve ser definido como <strong>NULL</strong> quando ele não puder codificar o próprio <strong>NULL</strong> (por exemplo, uma matriz de caracteres ou um número inteiro).</span><span class="sxs-lookup"><span data-stu-id="5f0fe-212">When setting a field, indicates the field should be set to <strong>NULL</strong> when the field cannot encode <strong>NULL</strong> itself (for example, a character array or an integer).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5f0fe-213"><strong>adFldTruncated</strong></span><span class="sxs-lookup"><span data-stu-id="5f0fe-213"><strong>adFldTruncated</strong></span></span></p></td>
<td><p><span data-ttu-id="5f0fe-214">quatro</span><span class="sxs-lookup"><span data-stu-id="5f0fe-214">4</span></span></p></td>
<td><p><span data-ttu-id="5f0fe-215">Os dados de comprimento variável ou os dígitos numéricos foram truncados.</span><span class="sxs-lookup"><span data-stu-id="5f0fe-215">Variable-length data or numeric digits were truncated.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5f0fe-216"><strong>adFldSignMismatch</strong></span><span class="sxs-lookup"><span data-stu-id="5f0fe-216"><strong>adFldSignMismatch</strong></span></span></p></td>
<td><p><span data-ttu-id="5f0fe-217">0,5</span><span class="sxs-lookup"><span data-stu-id="5f0fe-217">5</span></span></p></td>
<td><p><span data-ttu-id="5f0fe-218">O valor tem sinal e o tipo de dados variáveis não.</span><span class="sxs-lookup"><span data-stu-id="5f0fe-218">Value is signed and variable data type is unsigned.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5f0fe-219"><strong>adFldDataOverFlow</strong></span><span class="sxs-lookup"><span data-stu-id="5f0fe-219"><strong>adFldDataOverFlow</strong></span></span></p></td>
<td><p><span data-ttu-id="5f0fe-220">6</span><span class="sxs-lookup"><span data-stu-id="5f0fe-220">6</span></span></p></td>
<td><p><span data-ttu-id="5f0fe-221">O valor é maior do que pôde ser armazenado no tipo de dados variáveis.</span><span class="sxs-lookup"><span data-stu-id="5f0fe-221">Value is larger than could be stored in the variable data type.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5f0fe-222"><strong>adFldCantCreate</strong></span><span class="sxs-lookup"><span data-stu-id="5f0fe-222"><strong>adFldCantCreate</strong></span></span></p></td>
<td><p><span data-ttu-id="5f0fe-223">178</span><span class="sxs-lookup"><span data-stu-id="5f0fe-223">7</span></span></p></td>
<td><p><span data-ttu-id="5f0fe-224">Tipo de coluna desconhecida e campo já aberto.</span><span class="sxs-lookup"><span data-stu-id="5f0fe-224">Unknown column type and field already open.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5f0fe-225"><strong>adFldUnavailable</strong></span><span class="sxs-lookup"><span data-stu-id="5f0fe-225"><strong>adFldUnavailable</strong></span></span></p></td>
<td><p><span data-ttu-id="5f0fe-226">8</span><span class="sxs-lookup"><span data-stu-id="5f0fe-226">8</span></span></p></td>
<td><p><span data-ttu-id="5f0fe-227">Não foi possível determinar o valor de campo — por exemplo, em um novo campo sem alocação sem nenhum valor padrão.</span><span class="sxs-lookup"><span data-stu-id="5f0fe-227">Field value could not be determined — for example, on a new, unassigned field with no default value.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5f0fe-228"><strong>adFldPermissionDenied</strong></span><span class="sxs-lookup"><span data-stu-id="5f0fe-228"><strong>adFldPermissionDenied</strong></span></span></p></td>
<td><p><span data-ttu-id="5f0fe-229">241</span><span class="sxs-lookup"><span data-stu-id="5f0fe-229">9</span></span></p></td>
<td><p><span data-ttu-id="5f0fe-230">Durante uma atualização, não houve permissão para gravar dados.</span><span class="sxs-lookup"><span data-stu-id="5f0fe-230">When updating, no permission to write data.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5f0fe-231"><strong>adFldIntegrityViolation</strong></span><span class="sxs-lookup"><span data-stu-id="5f0fe-231"><strong>adFldIntegrityViolation</strong></span></span></p></td>
<td><p><span data-ttu-id="5f0fe-232">254</span><span class="sxs-lookup"><span data-stu-id="5f0fe-232">10</span></span></p></td>
<td><p><span data-ttu-id="5f0fe-233">Durante uma atualização, o valor de campo violaria a integridade da coluna.</span><span class="sxs-lookup"><span data-stu-id="5f0fe-233">When updating, field value would violate column integrity.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5f0fe-234"><strong>adFldSchemaViolation</strong></span><span class="sxs-lookup"><span data-stu-id="5f0fe-234"><strong>adFldSchemaViolation</strong></span></span></p></td>
<td><p><span data-ttu-id="5f0fe-235">11</span><span class="sxs-lookup"><span data-stu-id="5f0fe-235">11</span></span></p></td>
<td><p><span data-ttu-id="5f0fe-236">Durante uma atualização, o valor de campo violaria o esquema de coluna.</span><span class="sxs-lookup"><span data-stu-id="5f0fe-236">When updating, field value would violate column schema.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5f0fe-237"><strong>adFldBadStatus</strong></span><span class="sxs-lookup"><span data-stu-id="5f0fe-237"><strong>adFldBadStatus</strong></span></span></p></td>
<td><p><span data-ttu-id="5f0fe-238">3,6</span><span class="sxs-lookup"><span data-stu-id="5f0fe-238">12</span></span></p></td>
<td><p><span data-ttu-id="5f0fe-239">Durante uma atualização, um parâmetro de status inválido foi retornado.</span><span class="sxs-lookup"><span data-stu-id="5f0fe-239">When updating, invalid status parameter.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5f0fe-240"><strong>adFldDefault</strong></span><span class="sxs-lookup"><span data-stu-id="5f0fe-240"><strong>adFldDefault</strong></span></span></p></td>
<td><p><span data-ttu-id="5f0fe-241">Treze</span><span class="sxs-lookup"><span data-stu-id="5f0fe-241">13</span></span></p></td>
<td><p><span data-ttu-id="5f0fe-242">Durante uma atualização, um valor padrão foi utilizado.</span><span class="sxs-lookup"><span data-stu-id="5f0fe-242">When updating, a default value was used.</span></span></p></td>
</tr>
</tbody>
</table>

