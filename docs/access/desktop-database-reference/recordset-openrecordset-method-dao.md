---
title: Método Recordset.OpenRecordset (DAO)
TOCTitle: OpenRecordset Method
ms:assetid: 7d5ca4d5-5a0b-c0c8-d8e8-2c4e6c5f361f
ms:mtpsurl: https://msdn.microsoft.com/library/Ff196402(v=office.15)
ms:contentKeyID: 48545853
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Priority
ms.openlocfilehash: 11d525abdb7c5cbd4ef72e81d856d2abfc6a3045
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: pt-BR
ms.lasthandoff: 01/17/2019
ms.locfileid: "28702744"
---
# <a name="recordsetopenrecordset-method-dao"></a><span data-ttu-id="ecaa6-102">Método Recordset.OpenRecordset (DAO)</span><span class="sxs-lookup"><span data-stu-id="ecaa6-102">Recordset.OpenRecordset method (DAO)</span></span>

<span data-ttu-id="ecaa6-103">**Aplica-se a**: Access 2013, o Office 2013</span><span class="sxs-lookup"><span data-stu-id="ecaa6-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="ecaa6-104">Cria e anexa um novo objeto **[Recordset](recordset-object-dao.md)** à coleção **Recordsets**.</span><span class="sxs-lookup"><span data-stu-id="ecaa6-104">Creates a new **[Recordset](recordset-object-dao.md)** object and appends it to the **Recordsets** collection.</span></span>

## <a name="syntax"></a><span data-ttu-id="ecaa6-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="ecaa6-105">Syntax</span></span>

<span data-ttu-id="ecaa6-106">*expressão* . OpenRecordset (***tipo***, ***Opções***)</span><span class="sxs-lookup"><span data-stu-id="ecaa6-106">*expression* .OpenRecordset(***Type***, ***Options***)</span></span>

<span data-ttu-id="ecaa6-107">*expressão* Uma variável que representa um objeto **Recordset** .</span><span class="sxs-lookup"><span data-stu-id="ecaa6-107">*expression* A variable that represents a **Recordset** object.</span></span>

## <a name="parameters"></a><span data-ttu-id="ecaa6-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="ecaa6-108">Parameters</span></span>

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="ecaa6-109">Nome</span><span class="sxs-lookup"><span data-stu-id="ecaa6-109">Name</span></span></p></th>
<th><p><span data-ttu-id="ecaa6-110">Obrigatório/opcional</span><span class="sxs-lookup"><span data-stu-id="ecaa6-110">Required/optional</span></span></p></th>
<th><p><span data-ttu-id="ecaa6-111">Tipo de dados</span><span class="sxs-lookup"><span data-stu-id="ecaa6-111">Data type</span></span></p></th>
<th><p><span data-ttu-id="ecaa6-112">Descrição</span><span class="sxs-lookup"><span data-stu-id="ecaa6-112">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="ecaa6-113"><em>Name</em></span><span class="sxs-lookup"><span data-stu-id="ecaa6-113"><em>Name</em></span></span></p></td>
<td><p><span data-ttu-id="ecaa6-114">Obrigatório</span><span class="sxs-lookup"><span data-stu-id="ecaa6-114">Required</span></span></p></td>
<td><p><span data-ttu-id="ecaa6-115"><strong>String</strong></span><span class="sxs-lookup"><span data-stu-id="ecaa6-115"><strong>String</strong></span></span></p></td>
<td><p><span data-ttu-id="ecaa6-p101">A origem dos registros para o novo <strong>Recordset</strong>. A origem pode ser um nome de tabela, um nome de consulta ou uma instrução SQL que retorna registros. Para objetos de <strong>Recordset</strong> do tipo tabela nos mecanismos de banco de dados do Microsoft Access, a origem pode ser apenas um nome de tabela.  </span><span class="sxs-lookup"><span data-stu-id="ecaa6-p101">The source of the records for the new <strong>Recordset</strong>. The source can be a table name, a query name, or an SQL statement that returns records. For table-type <strong>Recordset</strong> objects in Microsoft Access database engine databases, the source can only be a table name.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ecaa6-119"><em>Type</em></span><span class="sxs-lookup"><span data-stu-id="ecaa6-119"><em>Type</em></span></span></p></td>
<td><p><span data-ttu-id="ecaa6-120">Opcional</span><span class="sxs-lookup"><span data-stu-id="ecaa6-120">Optional</span></span></p></td>
<td><p><span data-ttu-id="ecaa6-121"><strong>Variant</strong></span><span class="sxs-lookup"><span data-stu-id="ecaa6-121"><strong>Variant</strong></span></span></p></td>
<td><p><span data-ttu-id="ecaa6-122">Uma constante <strong><a href="recordsettypeenum-enumeration-dao.md">RecordsetTypeEnum</a></strong> que indica que tipo de <strong>Recordset</strong> abrir.</span><span class="sxs-lookup"><span data-stu-id="ecaa6-122">A <strong><a href="recordsettypeenum-enumeration-dao.md">RecordsetTypeEnum</a></strong> constant that indicates the type of <strong>Recordset</strong> to open.</span></span></p><p><span data-ttu-id="ecaa6-123"><strong>Observação</strong>: se você abrir um <STRONG>Recordset</STRONG> em um espaço de trabalho do Microsoft Access e você não especificar um tipo, <STRONG>OpenRecordset</STRONG> cria um <STRONG>Recordset</STRONG>do tipo tabela, se possível.</span><span class="sxs-lookup"><span data-stu-id="ecaa6-123"><strong>NOTE</strong>: If you open a <STRONG>Recordset</STRONG> in a Microsoft Access workspace and you don't specify a type, <STRONG>OpenRecordset</STRONG> creates a table-type <STRONG>Recordset</STRONG>, if possible.</span></span> <span data-ttu-id="ecaa6-124">Se você especificar uma consulta ou tabela vinculada, <STRONG>OpenRecordset</STRONG> cria um <STRONG>Recordset</STRONG>do tipo dynaset.</span><span class="sxs-lookup"><span data-stu-id="ecaa6-124">If you specify a linked table or query, <STRONG>OpenRecordset</STRONG> creates a dynaset-type <STRONG>Recordset</STRONG>.</span></span></p>
</td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ecaa6-125"><em>Options</em></span><span class="sxs-lookup"><span data-stu-id="ecaa6-125"><em>Options</em></span></span></p></td>
<td><p><span data-ttu-id="ecaa6-126">Opcional</span><span class="sxs-lookup"><span data-stu-id="ecaa6-126">Optional</span></span></p></td>
<td><p><span data-ttu-id="ecaa6-127"><strong>Variant</strong></span><span class="sxs-lookup"><span data-stu-id="ecaa6-127"><strong>Variant</strong></span></span></p></td>
<td><p><span data-ttu-id="ecaa6-128">Uma combinação de constantes <strong><a href="recordsetoptionenum-enumeration-dao.md">RecordsetOptionEnum</a></strong> que especifica as características do novo <strong>Recordset</strong>.</span><span class="sxs-lookup"><span data-stu-id="ecaa6-128">A combination of <strong><a href="recordsetoptionenum-enumeration-dao.md">RecordsetOptionEnum</a></strong> constants that specify characteristics of the new <strong>Recordset</strong>.</span></span></p></p><p><span data-ttu-id="ecaa6-129"><strong>Observação</strong>: as constantes <STRONG>dbConsistent</STRONG> e <STRONG>dbInconsistent</STRONG> são mutuamente exclusivos e usando os dois causará um erro.</span><span class="sxs-lookup"><span data-stu-id="ecaa6-129"><strong>NOTE</strong>: The constants <STRONG>dbConsistent</STRONG> and <STRONG>dbInconsistent</STRONG> are mutually exclusive, and using both causes an error.</span></span> <span data-ttu-id="ecaa6-130">Também fornecer um argumento lockedits quando opções usa a constante <STRONG>dbReadOnly</STRONG> causará um erro.</span><span class="sxs-lookup"><span data-stu-id="ecaa6-130">Supplying a lockedits argument when options uses the <STRONG>dbReadOnly</STRONG> constant also causes an error.</span></span></p>
</td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ecaa6-131"><em>LockEdit</em></span><span class="sxs-lookup"><span data-stu-id="ecaa6-131"><em>LockEdit</em></span></span></p></td>
<td><p><span data-ttu-id="ecaa6-132">Opcional</span><span class="sxs-lookup"><span data-stu-id="ecaa6-132">Optional</span></span></p></td>
<td><p><span data-ttu-id="ecaa6-133"><strong>Variant</strong></span><span class="sxs-lookup"><span data-stu-id="ecaa6-133"><strong>Variant</strong></span></span></p></td>
<td><p><span data-ttu-id="ecaa6-134">Uma constante <strong><a href="locktypeenum-enumeration-dao.md">LockTypeEnum</a></strong> que determina o bloqueio do <strong>Recordset</strong>.</span><span class="sxs-lookup"><span data-stu-id="ecaa6-134">A <strong><a href="locktypeenum-enumeration-dao.md">LockTypeEnum</a></strong> constant that determines the locking for the <strong>Recordset</strong>.</span></span></p></p><p><span data-ttu-id="ecaa6-135"><strong>Observação</strong>: você pode usar <STRONG>dbReadOnly</STRONG> no argumento options ou o argumento lockedits, mas não ambos.</span><span class="sxs-lookup"><span data-stu-id="ecaa6-135"><strong>NOTE</strong>: You can use <STRONG>dbReadOnly</STRONG> in either the options argument or the lockedits argument, but not both.</span></span> <span data-ttu-id="ecaa6-136">Se você usá-lo para ambos os argumentos, ocorrerá um erro em tempo de execução.</span><span class="sxs-lookup"><span data-stu-id="ecaa6-136">If you use it for both arguments, a run-time error occurs.</span></span></p>
</td>
</tr>
</tbody>
</table>


## <a name="return-value"></a><span data-ttu-id="ecaa6-137">Valor de retorno</span><span class="sxs-lookup"><span data-stu-id="ecaa6-137">Return value</span></span>

<span data-ttu-id="ecaa6-138">Recordset</span><span class="sxs-lookup"><span data-stu-id="ecaa6-138">Recordset</span></span>

## <a name="remarks"></a><span data-ttu-id="ecaa6-139">Comentários</span><span class="sxs-lookup"><span data-stu-id="ecaa6-139">Remarks</span></span>

<span data-ttu-id="ecaa6-p105">Normalmente, se o usuário obtém esse erro ao atualizar um registro, seu código deve atualizar o conteúdo dos campos e recuperar os valores modificados recentemente. Se o erro ocorrer ao excluir um registro, seu código poderá exibir os dados do novo registro para o usuário e uma mensagem indicando que os dados foram alterados recentemente. Nesse momento, seu código pode solicitar uma confirmação de que o usuário ainda deseja excluir o registro.</span><span class="sxs-lookup"><span data-stu-id="ecaa6-p105">Typically, if the user gets this error while updating a record, your code should refresh the contents of the fields and retrieve the newly modified values. If the error occurs while deleting a record, your code could display the new record data to the user and a message indicating that the data has recently changed. At this point, your code can request a confirmation that the user still wants to delete the record.</span></span>

<span data-ttu-id="ecaa6-143">Você também deverá usar a constante **dbSeeChanges** se abrir um **Recordset** em um espaço de trabalho ODBC conectado ao mecanismo de banco de dados do Microsoft Access em uma tabela do Microsoft SQL Server 6.0 (ou posterior), que tenha uma coluna IDENTITY; caso contrário, ocorrerá um erro.</span><span class="sxs-lookup"><span data-stu-id="ecaa6-143">You should also use the **dbSeeChanges** constant if you open a **Recordset** in a Microsoft Access database engine-connected ODBC workspace against a Microsoft SQL Server 6.0 (or later) table that has an IDENTITY column, otherwise an error may result.</span></span>

<span data-ttu-id="ecaa6-p106">Abrir mais de um **Recordset** em uma fonte de dados ODBC pode falhar porque a conexão está ocupada com uma chamada **OpenRecordset** anterior. Uma forma de contornar essa situação é preencher totalmente o **Recordset** usando o método **MoveLast** assim que o **Recordset** for aberto.</span><span class="sxs-lookup"><span data-stu-id="ecaa6-p106">Opening more than one **Recordset** on an ODBC data source may fail because the connection is busy with a prior **OpenRecordset** call. One way around this is to fully populate the **Recordset** by using the **MoveLast** method as soon as the **Recordset** is opened.</span></span>

<span data-ttu-id="ecaa6-146">Fechar um **Recordset** com o método **[Close](connection-close-method-dao.md)** o exclui automaticamente da coleção **Recordsets**.</span><span class="sxs-lookup"><span data-stu-id="ecaa6-146">Closing a **Recordset** with the **[Close](connection-close-method-dao.md)** method automatically deletes it from the **Recordsets** collection.</span></span>

> [!NOTE]
> <span data-ttu-id="ecaa6-147">Se a *fonte* refere-se a uma instrução SQL composto por uma cadeia de caracteres concatenada com um valor não inteiro e os parâmetros do sistema especificarem um caractere decimal que fora dos EUA, como uma vírgula (por exemplo, strSQL = "preço &gt; " &amp; lngPrice e lngPrice = 125,50), ocorrerá um erro ao tentar abrir o **Recordset**.</span><span class="sxs-lookup"><span data-stu-id="ecaa6-147">If *source* refers to an SQL statement composed of a string concatenated with a non-integer value, and the system parameters specify a non-U.S. decimal character such as a comma (for example, strSQL = "PRICE &gt; " &amp; lngPrice, and lngPrice = 125,50), an error occurs when you try to open the **Recordset**.</span></span> <span data-ttu-id="ecaa6-148">Isso ocorre porque durante a concatenação, o número é convertido para uma sequência utilizando o caractere decimal padrão do seu sistema, e o SQL aceita apenas caracteres decimais EUA.</span><span class="sxs-lookup"><span data-stu-id="ecaa6-148">This is because during concatenation, the number will be converted to a string using your system's default decimal character, and SQL only accepts U.S. decimal characters.</span></span>


