---
title: Método Connection.OpenRecordset (DAO)
TOCTitle: OpenRecordset Method
ms:assetid: 584a3e00-7589-90f1-aa6a-5d6116f0b5b6
ms:mtpsurl: https://msdn.microsoft.com/library/Ff194324(v=office.15)
ms:contentKeyID: 48544993
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: abbb7a4f58714aef0e085d0f37b5ee49378e0f51
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32295846"
---
# <a name="connectionopenrecordset-method-dao"></a><span data-ttu-id="716ec-102">Método Connection.OpenRecordset (DAO)</span><span class="sxs-lookup"><span data-stu-id="716ec-102">Connection.OpenRecordset method (DAO)</span></span>

<span data-ttu-id="716ec-103">**Aplica-se ao:** Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="716ec-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="716ec-104">Cria um novo objeto **[Conjunto de registros](recordset-object-dao.md)** e o acrescentar à coleção **Conjuntos de registros**.</span><span class="sxs-lookup"><span data-stu-id="716ec-104">Creates a new **[Recordset](recordset-object-dao.md)** object and appends it to the **Recordsets** collection.</span></span>

## <a name="syntax"></a><span data-ttu-id="716ec-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="716ec-105">Syntax</span></span>

<span data-ttu-id="716ec-106">*expressão* . OpenRecordset(***Name***, ***Type***, ***Options***, ***LockEdit***)</span><span class="sxs-lookup"><span data-stu-id="716ec-106">*expression* .OpenRecordset(***Name***, ***Type***, ***Options***, ***LockEdit***)</span></span>

<span data-ttu-id="716ec-107">*expressão* Uma variável que representa um objeto **Connection**.</span><span class="sxs-lookup"><span data-stu-id="716ec-107">*expression* A variable that represents a **Connection** object.</span></span>

## <a name="parameters"></a><span data-ttu-id="716ec-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="716ec-108">Parameters</span></span>

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="716ec-109">Nome</span><span class="sxs-lookup"><span data-stu-id="716ec-109">Name</span></span></p></th>
<th><p><span data-ttu-id="716ec-110">Necessária/opcional</span><span class="sxs-lookup"><span data-stu-id="716ec-110">Required/optional</span></span></p></th>
<th><p><span data-ttu-id="716ec-111">Tipo de dados</span><span class="sxs-lookup"><span data-stu-id="716ec-111">Data type</span></span></p></th>
<th><p><span data-ttu-id="716ec-112">Descrição</span><span class="sxs-lookup"><span data-stu-id="716ec-112">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="716ec-113"><em>Name</em></span><span class="sxs-lookup"><span data-stu-id="716ec-113"><em>Name</em></span></span></p></td>
<td><p><span data-ttu-id="716ec-114">Obrigatório</span><span class="sxs-lookup"><span data-stu-id="716ec-114">Required</span></span></p></td>
<td><p><span data-ttu-id="716ec-115"><strong>String</strong></span><span class="sxs-lookup"><span data-stu-id="716ec-115"><strong>String</strong></span></span></p></td>
<td><p><span data-ttu-id="716ec-p101">A origem dos registros para o novo <strong>Recordset</strong>. A origem pode ser um nome de tabela, um nome de consulta ou uma instrução SQL que retorna registros. Para objetos de <strong>Recordset</strong> do tipo tabela nos mecanismos de banco de dados do Microsoft Access, a origem pode ser apenas um nome de tabela.</span><span class="sxs-lookup"><span data-stu-id="716ec-p101">The source of the records for the new <strong>Recordset</strong>. The source can be a table name, a query name, or an SQL statement that returns records. For table-type <strong>Recordset</strong> objects in Microsoft Access database engine databases, the source can only be a table name.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="716ec-119"><em>Type</em></span><span class="sxs-lookup"><span data-stu-id="716ec-119"><em>Type</em></span></span></p></td>
<td><p><span data-ttu-id="716ec-120">Opcional</span><span class="sxs-lookup"><span data-stu-id="716ec-120">Optional</span></span></p></td>
<td><p><span data-ttu-id="716ec-121"><strong>Variant</strong></span><span class="sxs-lookup"><span data-stu-id="716ec-121"><strong>Variant</strong></span></span></p></td>
<td><p><span data-ttu-id="716ec-122">Uma constante <strong><a href="recordsettypeenum-enumeration-dao.md">RecordsetTypeEnum</a></strong> que indica que tipo de <strong>Recordset</strong> abrir.</span><span class="sxs-lookup"><span data-stu-id="716ec-122">A <strong><a href="recordsettypeenum-enumeration-dao.md">RecordsetTypeEnum</a></strong> constant that indicates the type of <strong>Recordset</strong> to open.</span></span></p><p><span data-ttu-id="716ec-123"><strong>OBSERVAÇÃO</strong>: Se você abrir um <strong>Conjunto de Registros</strong> em um espaço de trabalho do Microsoft Access e não especificar um tipo, o <strong>OpenRecordset</strong> criará uma tabela do tipo <strong>Conjunto de Registros</strong>, se possível.</span><span class="sxs-lookup"><span data-stu-id="716ec-123"><strong>NOTE</strong>: If you open a <strong>Recordset</strong> in a Microsoft Access workspace and you don't specify a type, <strong>OpenRecordset</strong> creates a table-type <strong>Recordset</strong>, if possible.</span></span> <span data-ttu-id="716ec-124">If you specify a linked table or query, <strong>OpenRecordset</strong> creates a dynaset-type <strong>Recordset</strong>.</span><span class="sxs-lookup"><span data-stu-id="716ec-124">If you specify a linked table or query, <strong>OpenRecordset</strong> creates a dynaset-type <strong>Recordset</strong>.</span></span></p>
</td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="716ec-125"><em>Opções</em></span><span class="sxs-lookup"><span data-stu-id="716ec-125"><em>Options</em></span></span></p></td>
<td><p><span data-ttu-id="716ec-126">Opcional</span><span class="sxs-lookup"><span data-stu-id="716ec-126">Optional</span></span></p></td>
<td><p><span data-ttu-id="716ec-127"><strong>Variant</strong></span><span class="sxs-lookup"><span data-stu-id="716ec-127"><strong>Variant</strong></span></span></p></td>
<td><p><span data-ttu-id="716ec-128">Uma combinação de constantes <strong><a href="recordsetoptionenum-enumeration-dao.md">RecordsetOptionEnum</a></strong> que especifica as características do novo <strong>Recordset</strong>.</span><span class="sxs-lookup"><span data-stu-id="716ec-128">A combination of <strong><a href="recordsetoptionenum-enumeration-dao.md">RecordsetOptionEnum</a></strong> constants that specify characteristics of the new <strong>Recordset</strong>.</span></span></p><p><span data-ttu-id="716ec-129"><strong>Observação</strong>: As constantes <strong>dbConsistent</strong> e <strong>dbInconsistent</strong> são mutuamente exclusivas e usar ambas causará um erro.</span><span class="sxs-lookup"><span data-stu-id="716ec-129"><strong>NOTE</strong>: The constants <strong>dbConsistent</strong> and <strong>dbInconsistent</strong> are mutually exclusive, and using both causes an error.</span></span> <span data-ttu-id="716ec-130">Fornecer um argumento lockedits quando as opções usarem a <strong>constante dbReadOnly</strong> também causará um erro.</span><span class="sxs-lookup"><span data-stu-id="716ec-130">Supplying a lockedits argument when options use the <strong>dbReadOnly</strong> constant also causes an error.</span></span></p>
</td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="716ec-131"><em>LockEdit</em></span><span class="sxs-lookup"><span data-stu-id="716ec-131"><em>LockEdit</em></span></span></p></td>
<td><p><span data-ttu-id="716ec-132">Opcional</span><span class="sxs-lookup"><span data-stu-id="716ec-132">Optional</span></span></p></td>
<td><p><span data-ttu-id="716ec-133"><strong>Variant</strong></span><span class="sxs-lookup"><span data-stu-id="716ec-133"><strong>Variant</strong></span></span></p></td>
<td><p><span data-ttu-id="716ec-134">Uma constante <strong><a href="locktypeenum-enumeration-dao.md">LockTypeEnum</a></strong> que determina o bloqueio do <strong>Recordset</strong>.</span><span class="sxs-lookup"><span data-stu-id="716ec-134">A <strong><a href="locktypeenum-enumeration-dao.md">LockTypeEnum</a></strong> constant that determines the locking for the <strong>Recordset</strong>.</span></span></p><p><span data-ttu-id="716ec-135"><strong>OBSERVAÇÃO</strong>: você pode usar a constante <strong>dbReadOnly</strong> tanto no argumento opções quanto no lockedits, mas não em ambos.</span><span class="sxs-lookup"><span data-stu-id="716ec-135"><strong>NOTE</strong>: You can use <strong>dbReadOnly</strong> in either the options argument or the lockedits argument, but not both.</span></span> <span data-ttu-id="716ec-136">Se você usá-la para ambos argumentos, ocorrerá um erro de tempo de execução.</span><span class="sxs-lookup"><span data-stu-id="716ec-136">If you use it for both arguments, a run-time error occurs.</span></span></p>
</td>
</tr>
</tbody>
</table>


## <a name="return-value"></a><span data-ttu-id="716ec-137">Valor de retorno</span><span class="sxs-lookup"><span data-stu-id="716ec-137">Return value</span></span>

<span data-ttu-id="716ec-138">Conjunto de Registros</span><span class="sxs-lookup"><span data-stu-id="716ec-138">Recordset</span></span>

## <a name="remarks"></a><span data-ttu-id="716ec-139">Comentários</span><span class="sxs-lookup"><span data-stu-id="716ec-139">Remarks</span></span>

<span data-ttu-id="716ec-p105">Normalmente, se o usuário receber este erro durante a atualização de um registro, seu código deverá atualizar o conteúdo dos campos e recuperar os valores modificados recentemente. Se o erro ocorrer durante a exclusão de um registro, o código poderá exibir os novos dados de registro para o usuário e uma mensagem indicando que os dados foram alterados recentemente. Nesse momento, seu código pode solicitar uma confirmação de que o usuário ainda deseja excluir o registro.</span><span class="sxs-lookup"><span data-stu-id="716ec-p105">Typically, if the user gets this error while updating a record, your code should refresh the contents of the fields and retrieve the newly modified values. If the error occurs while deleting a record, your code could display the new record data to the user and a message indicating that the data has recently changed. At this point, your code can request a confirmation that the user still wants to delete the record.</span></span>

<span data-ttu-id="716ec-143">Você também deve usar a constante **dbSeeChanges** se for abrir um **Recordset** em um espaço de trabalho ODBC conectado ao mecanismo do banco de dados do Microsoft Access versus uma tabela do Microsoft SQL Server 6.0 (ou posterior) com uma coluna IDENTIDADE, caso contrário pode resultar em um erro.</span><span class="sxs-lookup"><span data-stu-id="716ec-143">You should also use the **dbSeeChanges** constant if you open a **Recordset** in a Microsoft Access database engine-connected ODBC workspace against a Microsoft SQL Server 6.0 (or later) table that has an IDENTITY column, otherwise an error may result.</span></span>

<span data-ttu-id="716ec-p106">Abrir mais de um  **Recordset** em uma origem de dados ODBC pode falhar porque a conexão está ocupada com uma chamada **OpenRecordset** anterior. Uma maneira de evitar isso é preenchendo completamente o **Recordset** usando o método **MoveLast** assim que o **Recordset** for aberto.</span><span class="sxs-lookup"><span data-stu-id="716ec-p106">Opening more than one **Recordset** on an ODBC data source may fail because the connection is busy with a prior **OpenRecordset** call. One way around this is to fully populate the **Recordset** by using the **MoveLast** method as soon as the **Recordset** is opened.</span></span>

<span data-ttu-id="716ec-146">Fechar o **Recordset** com o método **[Close](connection-close-method-dao.md)** o exclui automaticamente da coleção de **Recordsets**.</span><span class="sxs-lookup"><span data-stu-id="716ec-146">Closing a **Recordset** with the **[Close](connection-close-method-dao.md)** method automatically deletes it from the **Recordsets** collection.</span></span>

> [!NOTE]
> <span data-ttu-id="716ec-147">Se a *fonte* se referir a uma instrução SQL composta por uma sequência concatenada e com um valor não inteiro, e se os parâmetros do sistema especificarem um caractere decimal não-EUA, como uma vírgula (por exemplo, strSQL = "PRICE &gt; " &amp; lngPrice e lngPrice = 125,50), ocorrerá um erro ao tentar abrir o **Conjunto de Registros**.</span><span class="sxs-lookup"><span data-stu-id="716ec-147">If *source* refers to an SQL statement composed of a string concatenated with a non-integer value, and the system parameters specify a non-U.S. decimal character such as a comma (for example, strSQL = "PRICE &gt; " &amp; lngPrice, and lngPrice = 125,50), an error occurs when you try to open the **Recordset**.</span></span> <span data-ttu-id="716ec-148">Isso se deve ao fato de que, durante a concatenação, o número é convertido em uma cadeia de caracteres usando o caractere decimal padrão do seu sistema, e o SQL aceita apenas caracteres decimais americanos.</span><span class="sxs-lookup"><span data-stu-id="716ec-148">This is because during concatenation, the number will be converted to a string using your system's default decimal character, and SQL only accepts U.S. decimal characters.</span></span>


