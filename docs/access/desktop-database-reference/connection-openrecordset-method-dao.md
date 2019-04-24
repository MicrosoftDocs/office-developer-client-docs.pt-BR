---
title: Método Connection. OpenRecordset (DAO)
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
# <a name="connectionopenrecordset-method-dao"></a><span data-ttu-id="51022-102">Método Connection. OpenRecordset (DAO)</span><span class="sxs-lookup"><span data-stu-id="51022-102">Connection.OpenRecordset method (DAO)</span></span>

<span data-ttu-id="51022-103">**Aplica-se ao:** Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="51022-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="51022-104">Cria e anexa um novo objeto **[Recordset](recordset-object-dao.md)** à coleção **Recordsets**.</span><span class="sxs-lookup"><span data-stu-id="51022-104">Creates a new **[Recordset](recordset-object-dao.md)** object and appends it to the **Recordsets** collection.</span></span>

## <a name="syntax"></a><span data-ttu-id="51022-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="51022-105">Syntax</span></span>

<span data-ttu-id="51022-106">*expressão* . OpenRecordset (***nome***, ***tipo***, ***Opções***, ***LockEdit***)</span><span class="sxs-lookup"><span data-stu-id="51022-106">*expression* .OpenRecordset(***Name***, ***Type***, ***Options***, ***LockEdit***)</span></span>

<span data-ttu-id="51022-107">*expressão* Uma variável que representa um objeto **Connection** .</span><span class="sxs-lookup"><span data-stu-id="51022-107">*expression* A variable that represents a **Connection** object.</span></span>

## <a name="parameters"></a><span data-ttu-id="51022-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="51022-108">Parameters</span></span>

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="51022-109">Nome</span><span class="sxs-lookup"><span data-stu-id="51022-109">Name</span></span></p></th>
<th><p><span data-ttu-id="51022-110">Obrigatório/opcional</span><span class="sxs-lookup"><span data-stu-id="51022-110">Required/optional</span></span></p></th>
<th><p><span data-ttu-id="51022-111">Tipo de dados</span><span class="sxs-lookup"><span data-stu-id="51022-111">Data type</span></span></p></th>
<th><p><span data-ttu-id="51022-112">Descrição</span><span class="sxs-lookup"><span data-stu-id="51022-112">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="51022-113"><em>Nome</em></span><span class="sxs-lookup"><span data-stu-id="51022-113"><em>Name</em></span></span></p></td>
<td><p><span data-ttu-id="51022-114">Obrigatório</span><span class="sxs-lookup"><span data-stu-id="51022-114">Required</span></span></p></td>
<td><p><span data-ttu-id="51022-115"><strong>String</strong></span><span class="sxs-lookup"><span data-stu-id="51022-115"><strong>String</strong></span></span></p></td>
<td><p><span data-ttu-id="51022-p101">A origem dos registros para o novo <strong>Recordset</strong>. A origem pode ser um nome de tabela, um nome de consulta ou uma instrução SQL que retorna registros. Para objetos de <strong>Recordset</strong> do tipo tabela nos mecanismos de banco de dados do Microsoft Access, a origem pode ser apenas um nome de tabela.  </span><span class="sxs-lookup"><span data-stu-id="51022-p101">The source of the records for the new <strong>Recordset</strong>. The source can be a table name, a query name, or an SQL statement that returns records. For table-type <strong>Recordset</strong> objects in Microsoft Access database engine databases, the source can only be a table name.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="51022-119"><em>Type</em></span><span class="sxs-lookup"><span data-stu-id="51022-119"><em>Type</em></span></span></p></td>
<td><p><span data-ttu-id="51022-120">Opcional</span><span class="sxs-lookup"><span data-stu-id="51022-120">Optional</span></span></p></td>
<td><p><span data-ttu-id="51022-121"><strong>Variant</strong></span><span class="sxs-lookup"><span data-stu-id="51022-121"><strong>Variant</strong></span></span></p></td>
<td><p><span data-ttu-id="51022-122">Uma constante <strong><a href="recordsettypeenum-enumeration-dao.md">RecordsetTypeEnum</a></strong> que indica que tipo de <strong>Recordset</strong> abrir.</span><span class="sxs-lookup"><span data-stu-id="51022-122">A <strong><a href="recordsettypeenum-enumeration-dao.md">RecordsetTypeEnum</a></strong> constant that indicates the type of <strong>Recordset</strong> to open.</span></span></p><p><span data-ttu-id="51022-123"><strong>Observação</strong>: se você abrir um <strong>Recordset</strong> em um espaço de trabalho do Microsoft Access e não especificar um tipo, <strong>OpenRecordset</strong> criará um <strong>Recordset</strong>do tipo tabela, se possível.</span><span class="sxs-lookup"><span data-stu-id="51022-123"><strong>NOTE</strong>: If you open a <strong>Recordset</strong> in a Microsoft Access workspace and you don't specify a type, <strong>OpenRecordset</strong> creates a table-type <strong>Recordset</strong>, if possible.</span></span> <span data-ttu-id="51022-124">If you specify a linked table or query, <strong>OpenRecordset</strong> creates a dynaset-type <strong>Recordset</strong>.</span><span class="sxs-lookup"><span data-stu-id="51022-124">If you specify a linked table or query, <strong>OpenRecordset</strong> creates a dynaset-type <strong>Recordset</strong>.</span></span></p>
</td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="51022-125"><em>Options</em></span><span class="sxs-lookup"><span data-stu-id="51022-125"><em>Options</em></span></span></p></td>
<td><p><span data-ttu-id="51022-126">Opcional</span><span class="sxs-lookup"><span data-stu-id="51022-126">Optional</span></span></p></td>
<td><p><span data-ttu-id="51022-127"><strong>Variant</strong></span><span class="sxs-lookup"><span data-stu-id="51022-127"><strong>Variant</strong></span></span></p></td>
<td><p><span data-ttu-id="51022-128">Uma combinação de constantes <strong><a href="recordsetoptionenum-enumeration-dao.md">RecordsetOptionEnum</a></strong> que especifica as características do novo <strong>Recordset</strong>.</span><span class="sxs-lookup"><span data-stu-id="51022-128">A combination of <strong><a href="recordsetoptionenum-enumeration-dao.md">RecordsetOptionEnum</a></strong> constants that specify characteristics of the new <strong>Recordset</strong>.</span></span></p><p><span data-ttu-id="51022-129"><strong>Observação</strong>: as constantes <strong>dbConsistent</strong> e <strong>dbInconsistent</strong> são mutuamente exclusivas e o uso de ambas causa um erro.</span><span class="sxs-lookup"><span data-stu-id="51022-129"><strong>NOTE</strong>: The constants <strong>dbConsistent</strong> and <strong>dbInconsistent</strong> are mutually exclusive, and using both causes an error.</span></span> <span data-ttu-id="51022-130">Fornecer um argumento LockEdits quando as opções usam a constante <strong>dbReadOnly</strong> também causa um erro.</span><span class="sxs-lookup"><span data-stu-id="51022-130">Supplying a lockedits argument when options use the <strong>dbReadOnly</strong> constant also causes an error.</span></span></p>
</td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="51022-131"><em>LockEdit</em></span><span class="sxs-lookup"><span data-stu-id="51022-131"><em>LockEdit</em></span></span></p></td>
<td><p><span data-ttu-id="51022-132">Opcional</span><span class="sxs-lookup"><span data-stu-id="51022-132">Optional</span></span></p></td>
<td><p><span data-ttu-id="51022-133"><strong>Variant</strong></span><span class="sxs-lookup"><span data-stu-id="51022-133"><strong>Variant</strong></span></span></p></td>
<td><p><span data-ttu-id="51022-134">Uma constante <strong><a href="locktypeenum-enumeration-dao.md">LockTypeEnum</a></strong> que determina o bloqueio do <strong>Recordset</strong>.</span><span class="sxs-lookup"><span data-stu-id="51022-134">A <strong><a href="locktypeenum-enumeration-dao.md">LockTypeEnum</a></strong> constant that determines the locking for the <strong>Recordset</strong>.</span></span></p><p><span data-ttu-id="51022-135"><strong>Observação</strong>: você pode usar <strong>dbReadOnly</strong> no argumento Options ou no argumento LockEdits, mas não em ambos.</span><span class="sxs-lookup"><span data-stu-id="51022-135"><strong>NOTE</strong>: You can use <strong>dbReadOnly</strong> in either the options argument or the lockedits argument, but not both.</span></span> <span data-ttu-id="51022-136">If you use it for both arguments, a run-time error occurs.</span><span class="sxs-lookup"><span data-stu-id="51022-136">If you use it for both arguments, a run-time error occurs.</span></span></p>
</td>
</tr>
</tbody>
</table>


## <a name="return-value"></a><span data-ttu-id="51022-137">Valor de retorno</span><span class="sxs-lookup"><span data-stu-id="51022-137">Return value</span></span>

<span data-ttu-id="51022-138">Recordset</span><span class="sxs-lookup"><span data-stu-id="51022-138">Recordset</span></span>

## <a name="remarks"></a><span data-ttu-id="51022-139">Comentários</span><span class="sxs-lookup"><span data-stu-id="51022-139">Remarks</span></span>

<span data-ttu-id="51022-p105">Normalmente, se o usuário obtém esse erro ao atualizar um registro, seu código deve atualizar o conteúdo dos campos e recuperar os valores modificados recentemente. Se o erro ocorrer ao excluir um registro, seu código poderá exibir os dados do novo registro para o usuário e uma mensagem indicando que os dados foram alterados recentemente. Nesse momento, seu código pode solicitar uma confirmação de que o usuário ainda deseja excluir o registro.</span><span class="sxs-lookup"><span data-stu-id="51022-p105">Typically, if the user gets this error while updating a record, your code should refresh the contents of the fields and retrieve the newly modified values. If the error occurs while deleting a record, your code could display the new record data to the user and a message indicating that the data has recently changed. At this point, your code can request a confirmation that the user still wants to delete the record.</span></span>

<span data-ttu-id="51022-143">Você também deverá usar a constante **dbSeeChanges** se abrir um **Recordset** em um espaço de trabalho ODBC conectado ao mecanismo de banco de dados do Microsoft Access em uma tabela do Microsoft SQL Server 6.0 (ou posterior), que tenha uma coluna IDENTITY; caso contrário, ocorrerá um erro.</span><span class="sxs-lookup"><span data-stu-id="51022-143">You should also use the **dbSeeChanges** constant if you open a **Recordset** in a Microsoft Access database engine-connected ODBC workspace against a Microsoft SQL Server 6.0 (or later) table that has an IDENTITY column, otherwise an error may result.</span></span>

<span data-ttu-id="51022-p106">Abrir mais de um **Recordset** em uma fonte de dados ODBC pode falhar porque a conexão está ocupada com uma chamada **OpenRecordset** anterior. Uma forma de contornar essa situação é preencher totalmente o **Recordset** usando o método **MoveLast** assim que o **Recordset** for aberto.</span><span class="sxs-lookup"><span data-stu-id="51022-p106">Opening more than one **Recordset** on an ODBC data source may fail because the connection is busy with a prior **OpenRecordset** call. One way around this is to fully populate the **Recordset** by using the **MoveLast** method as soon as the **Recordset** is opened.</span></span>

<span data-ttu-id="51022-146">Fechar um **Recordset** com o método **[Close](connection-close-method-dao.md)** o exclui automaticamente da coleção **Recordsets**.</span><span class="sxs-lookup"><span data-stu-id="51022-146">Closing a **Recordset** with the **[Close](connection-close-method-dao.md)** method automatically deletes it from the **Recordsets** collection.</span></span>

> [!NOTE]
> <span data-ttu-id="51022-147">Se *Source* se refere a uma instrução SQL composta de uma cadeia de caracteres concatenada com um valor não inteiro e os parâmetros do sistema especificam um caractere não-U. decimal, como vírgula (por exemplo, strSQL = "Price &gt; " &amp; lngPrice e lngPrice = 125, 50), ocorrerá um erro quando você tentar abrir o **Recordset**.</span><span class="sxs-lookup"><span data-stu-id="51022-147">If *source* refers to an SQL statement composed of a string concatenated with a non-integer value, and the system parameters specify a non-U.S. decimal character such as a comma (for example, strSQL = "PRICE &gt; " &amp; lngPrice, and lngPrice = 125,50), an error occurs when you try to open the **Recordset**.</span></span> <span data-ttu-id="51022-148">Isso se deve ao fato de que, durante a concatenação, o número é convertido em uma cadeia de caracteres usando o caractere decimal padrão do seu sistema, e o SQL aceita apenas caracteres decimais americanos.</span><span class="sxs-lookup"><span data-stu-id="51022-148">This is because during concatenation, the number will be converted to a string using your system's default decimal character, and SQL only accepts U.S. decimal characters.</span></span>


