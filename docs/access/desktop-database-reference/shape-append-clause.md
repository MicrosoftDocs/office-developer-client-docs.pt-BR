---
title: Cláusula Shape Append
TOCTitle: Shape Append Clause
ms:assetid: 8f29afc3-fb93-4439-b67b-cad0eed0bda9
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249633(v=office.15)
ms:contentKeyID: 48546301
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: cb8e60c52ded359350adff737807c3e0f92cb7c4
ms.sourcegitcommit: 801b1b54786f7b0e5b0d35466e7ae8d1e840b26f
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/31/2018
ms.locfileid: "25862119"
---
# <a name="shape-append-clause"></a><span data-ttu-id="f761f-102">Cláusula Shape Append</span><span class="sxs-lookup"><span data-stu-id="f761f-102">Shape Append Clause</span></span>


<span data-ttu-id="f761f-103">**Aplica-se a**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="f761f-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="f761f-p101">A cláusula APPEND do comando shape acrescenta uma ou mais colunas a um **Recordset**. Em geral, essas colunas referem-se a capítulos, que se referem a um **Recordset** filho .</span><span class="sxs-lookup"><span data-stu-id="f761f-p101">The shape command APPEND clause appends a column or columns to a **Recordset**. Often these columns are chapter columns, which refer to a child **Recordset**.</span></span>

## <a name="syntax"></a><span data-ttu-id="f761f-106">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="f761f-106">Syntax</span></span>

```vb 
 
SHAPE [parent-command [[AS] parent-alias]] APPEND column-list
```

## <a name="description"></a><span data-ttu-id="f761f-107">Descrição</span><span class="sxs-lookup"><span data-stu-id="f761f-107">Description</span></span>

<span data-ttu-id="f761f-108">As partes dessa cláusula são as seguintes:</span><span class="sxs-lookup"><span data-stu-id="f761f-108">The parts of this clause are as follows:</span></span>

- <span data-ttu-id="f761f-109">*parent-command*</span><span class="sxs-lookup"><span data-stu-id="f761f-109">*parent-command*</span></span>

- <span data-ttu-id="f761f-110">Zero ou uma das opções a seguir (você pode omitir o *parent-command* completamente):</span><span class="sxs-lookup"><span data-stu-id="f761f-110">Zero or one of the following (you may omit the *parent-command* entirely):</span></span>
    
  - <span data-ttu-id="f761f-p102">Um comando de provedor entre chaves ("{}") que retorna um objeto **Recordset**. O comando é emitido para o provedor de dados subjacente, e sua sintaxe depende dos requisitos desse provedor. Em geral, será usada a linguagem SQL, embora o ADO não exija nenhuma linguagem de consulta específica.</span><span class="sxs-lookup"><span data-stu-id="f761f-p102">A provider command within curly braces ("{}") that returns a **Recordset** object. The command is issued to the underlying data provider, and its syntax depends on the requirements of that provider. This will typically be the SQL language, although ADO does not require any particular query language.</span></span>
    
  - <span data-ttu-id="f761f-114">Um outro comando shape entre parênteses.</span><span class="sxs-lookup"><span data-stu-id="f761f-114">Another shape command embedded in parentheses.</span></span>
    
  - <span data-ttu-id="f761f-115">A palavra-chave TABLE, seguida do nome de uma tabela no provedor de dados.</span><span class="sxs-lookup"><span data-stu-id="f761f-115">The TABLE keyword, followed by the name of a table in the data provider.</span></span>

- <span data-ttu-id="f761f-116">*parent-alias*</span><span class="sxs-lookup"><span data-stu-id="f761f-116">*parent-alias*</span></span>

  - <span data-ttu-id="f761f-117">Um alias opcional que se refere ao **Recordset** pai.</span><span class="sxs-lookup"><span data-stu-id="f761f-117">An optional alias that refers to the parent **Recordset**.</span></span>

- <span data-ttu-id="f761f-118">*column-list*</span><span class="sxs-lookup"><span data-stu-id="f761f-118">*column-list*</span></span>

  - <span data-ttu-id="f761f-119">Um ou mais itens a seguir:</span><span class="sxs-lookup"><span data-stu-id="f761f-119">One or more of the following:</span></span>
    
    - <span data-ttu-id="f761f-120">Uma coluna agregada.</span><span class="sxs-lookup"><span data-stu-id="f761f-120">An aggregate column.</span></span>
    
    - <span data-ttu-id="f761f-121">Uma coluna calculada.</span><span class="sxs-lookup"><span data-stu-id="f761f-121">A calculated column.</span></span>
    
    - <span data-ttu-id="f761f-122">Uma nova coluna criada com a cláusula NEW.</span><span class="sxs-lookup"><span data-stu-id="f761f-122">A new column created with the NEW clause.</span></span>
    
    - <span data-ttu-id="f761f-p103">Uma coluna de capítulo. Uma definição dessa coluna é exibida entre parênteses ("()"). Consulte a sintaxe a seguir:</span><span class="sxs-lookup"><span data-stu-id="f761f-p103">A chapter column. A chapter column definition is enclosed in parentheses ("()"). See syntax below:</span></span>


        ```vb 
        
        SHAPE [parent-command [[AS] parent-alias]] 
        APPEND (child-recordset [ [[AS] child-alias] 
        RELATE parent-column TO child-column | PARAMETER param-number, ... ]) 
        [[AS] chapter-alias] 
        [, ... ] 
        ```

- <span data-ttu-id="f761f-126">*child-recordset*</span><span class="sxs-lookup"><span data-stu-id="f761f-126">*child-recordset*</span></span>

  - <span data-ttu-id="f761f-p104">Um comando de provedor entre chaves ("{}") que retorna um objeto **Recordset**. O comando é emitido para o provedor de dados subjacente, e sua sintaxe depende dos requisitos desse provedor. Em geral, será usada a linguagem SQL, embora o ADO não exija nenhuma linguagem de consulta específica.</span><span class="sxs-lookup"><span data-stu-id="f761f-p104">A provider command within curly braces ("{}") that returns a **Recordset** object. The command is issued to the underlying data provider, and its syntax depends on the requirements of that provider. This will typically be the SQL language, although ADO does not require any particular query language.</span></span>
    
  - <span data-ttu-id="f761f-130">Um outro comando shape entre parênteses.</span><span class="sxs-lookup"><span data-stu-id="f761f-130">Another shape command embedded in parentheses.</span></span>
    
  - <span data-ttu-id="f761f-131">O nome de um **Recordset** com formato existente.</span><span class="sxs-lookup"><span data-stu-id="f761f-131">The name of an existing shaped **Recordset**.</span></span>
    
  - <span data-ttu-id="f761f-132">A palavra-chave TABLE, seguida do nome de uma tabela no provedor de dados.</span><span class="sxs-lookup"><span data-stu-id="f761f-132">The TABLE keyword, followed by the name of a table in the data provider.</span></span>

- <span data-ttu-id="f761f-133">*child-alias*</span><span class="sxs-lookup"><span data-stu-id="f761f-133">*child-alias*</span></span>

  - <span data-ttu-id="f761f-134">Um alias que se refere ao **Recordset** filho.</span><span class="sxs-lookup"><span data-stu-id="f761f-134">An alias that refers to the child **Recordset**.</span></span>

- <span data-ttu-id="f761f-135">*parent-column*</span><span class="sxs-lookup"><span data-stu-id="f761f-135">*parent-column*</span></span>

  - <span data-ttu-id="f761f-136">Uma coluna em **Recordset** retornada pelo *parent-command.*</span><span class="sxs-lookup"><span data-stu-id="f761f-136">A column in the **Recordset** returned by the *parent-command.*</span></span>

- <span data-ttu-id="f761f-137">*child-column*</span><span class="sxs-lookup"><span data-stu-id="f761f-137">*child-column*</span></span>

  - <span data-ttu-id="f761f-138">Uma coluna em **Recordset** retornada por *child-command.*</span><span class="sxs-lookup"><span data-stu-id="f761f-138">A column in the **Recordset** returned by the *child-command*.</span></span>

- <span data-ttu-id="f761f-139">*param-number*</span><span class="sxs-lookup"><span data-stu-id="f761f-139">*param-number*</span></span>

  - <span data-ttu-id="f761f-140">Consulte [Operação dos comandos com parâmetros](operation-of-parameterized-commands.md).</span><span class="sxs-lookup"><span data-stu-id="f761f-140">See [Operation of Parameterized Commands](operation-of-parameterized-commands.md).</span></span>

- <span data-ttu-id="f761f-141">*chapter-alias*</span><span class="sxs-lookup"><span data-stu-id="f761f-141">*chapter-alias*</span></span>

  - <span data-ttu-id="f761f-142">Um alias que se refere à coluna de capítulo acrescentada ao pai.</span><span class="sxs-lookup"><span data-stu-id="f761f-142">An alias that refers to the chapter column appended to the parent.</span></span>


> [!NOTE]
> - <span data-ttu-id="f761f-143">A cláusula _"parent-column TO filho-column"_ na verdade é uma lista, onde cada relação definida é separada por uma vírgula.</span><span class="sxs-lookup"><span data-stu-id="f761f-143">The _"parent-column TO child-column"_ clause is actually a list, where each relation defined is separated by a comma.</span></span>
> - <span data-ttu-id="f761f-144">[!OBSERVAçãO] A cláusula após a palavra-chave APPEND na verdade é uma lista, na qual cada cláusula é separada por uma vírgula e define uma outra coluna a ser acrescentada ao pai.</span><span class="sxs-lookup"><span data-stu-id="f761f-144">The clause after the APPEND keyword is actually a list, where each clause is separated by a comma and defines another column to be appended to the parent.</span></span>



## <a name="remarks"></a><span data-ttu-id="f761f-145">Comentários</span><span class="sxs-lookup"><span data-stu-id="f761f-145">Remarks</span></span>

<span data-ttu-id="f761f-p105">Quando você construir os comandos de provedor a partir da entrada do usuário como parte de um comando SHAPE, SHAPE tratará o comando de provedor fornecido pelo usuário como uma sequência opaca e o passará fielmente ao provedor. Por exemplo, no comando SHAPE a seguir,</span><span class="sxs-lookup"><span data-stu-id="f761f-p105">When you construct provider commands from user input as part of a SHAPE command, SHAPE will treat the user-supplied a provider command as an opaque string and pass them faithfully to the provider. For example, in the following SHAPE command,</span></span>

```vb 
 
SHAPE {select * from t1} APPEND ({select * from t2} RELATE k1 TO k2) 
```

<span data-ttu-id="f761f-148">FORMA irá executar dois comandos: selecione \* de t1 e (selecione \* do t2 relacionar k1 para k2).</span><span class="sxs-lookup"><span data-stu-id="f761f-148">SHAPE will execute two commands: select \* from t1 and (select \* from t2 RELATE k1 TO k2).</span></span> <span data-ttu-id="f761f-149">Se o usuário emitir um comando composto contendo vários comandos de provedor separados por ponto-e-vírgula, SHAPE não conseguirá diferenciar.</span><span class="sxs-lookup"><span data-stu-id="f761f-149">If the user supplies a compound command consisting of multiple provider commands separated by semicolons, SHAPE is not able to discern the difference.</span></span> <span data-ttu-id="f761f-150">Portanto, no comando SHAPE a seguir,</span><span class="sxs-lookup"><span data-stu-id="f761f-150">So in the following SHAPE command,</span></span>

```vb 
 
SHAPE {select * from t1; drop table t1} APPEND ({select * from t2} RELATE k1 TO k2) 
```

<span data-ttu-id="f761f-151">Executa de forma selecionar \* de t1; Descartar tabela t1 e (selecione \* do t2 relacionar k1 para k2), não percebendo que t1 da tabela de recebimento é uma separado e neste comando perigoso, caso, o provedor.</span><span class="sxs-lookup"><span data-stu-id="f761f-151">SHAPE executes select \* from t1; drop table t1 and (select \* from t2 RELATE k1 TO k2), not realizing that drop table t1 is a separate and in this case, dangerous, provider command.</span></span> <span data-ttu-id="f761f-152">Os aplicativos devem sempre validar a entrada do usuário para impedir possíveis ataques de hacker como esse.</span><span class="sxs-lookup"><span data-stu-id="f761f-152">Applications must always validate the user input to prevent such potential hacker attacks from happening.</span></span>

<span data-ttu-id="f761f-153">Esta seção inclui os seguintes tópicos:</span><span class="sxs-lookup"><span data-stu-id="f761f-153">This section includes the following topics:</span></span>

- [<span data-ttu-id="f761f-154">Operação de comandos não parametrizados</span><span class="sxs-lookup"><span data-stu-id="f761f-154">Operation of Non-Parameterized Commands</span></span>](operation-of-non-parameterized-commands.md)

- [<span data-ttu-id="f761f-155">Operação de comandos parametrizados</span><span class="sxs-lookup"><span data-stu-id="f761f-155">Operation of Parameterized Commands</span></span>](operation-of-parameterized-commands.md)

- [<span data-ttu-id="f761f-156">Comandos híbridos</span><span class="sxs-lookup"><span data-stu-id="f761f-156">Hybrid Commands</span></span>](hybrid-commands.md)

- [<span data-ttu-id="f761f-157">Cláusulas COMPUTE de intervenção de forma</span><span class="sxs-lookup"><span data-stu-id="f761f-157">Intervening Shape COMPUTE Clauses</span></span>](intervening-shape-compute-clauses.md)