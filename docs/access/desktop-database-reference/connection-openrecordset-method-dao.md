---
title: Método Connection.OpenRecordset (DAO)
TOCTitle: OpenRecordset Method
ms:assetid: 584a3e00-7589-90f1-aa6a-5d6116f0b5b6
ms:mtpsurl: https://msdn.microsoft.com/library/Ff194324(v=office.15)
ms:contentKeyID: 48544993
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 52dcd2c09d04ca0cb7078c946edc4525fe49280d
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/09/2018
ms.locfileid: "25463377"
---
# <a name="connectionopenrecordset-method-dao"></a><span data-ttu-id="17754-102">Método Connection.OpenRecordset (DAO)</span><span class="sxs-lookup"><span data-stu-id="17754-102">Connection.OpenRecordset Method (DAO)</span></span>


<span data-ttu-id="17754-103">**Aplica-se a**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="17754-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="17754-104">Cria e anexa um novo objeto **[Recordset](recordset-object-dao.md)** à coleção **Recordsets**.</span><span class="sxs-lookup"><span data-stu-id="17754-104">Creates a new **[Recordset](recordset-object-dao.md)** object and appends it to the **Recordsets** collection.</span></span>

## <a name="syntax"></a><span data-ttu-id="17754-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="17754-105">Syntax</span></span>

<span data-ttu-id="17754-106">*expressão* . OpenRecordset (***nome***, ***tipo***, ***Opções***, ***LockEdit***)</span><span class="sxs-lookup"><span data-stu-id="17754-106">*expression* .OpenRecordset(***Name***, ***Type***, ***Options***, ***LockEdit***)</span></span>

<span data-ttu-id="17754-107">*expressão* Uma variável que representa um objeto de **Conexão** .</span><span class="sxs-lookup"><span data-stu-id="17754-107">*expression* A variable that represents a **Connection** object.</span></span>

### <a name="parameters"></a><span data-ttu-id="17754-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="17754-108">Parameters</span></span>

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="17754-109">Nome</span><span class="sxs-lookup"><span data-stu-id="17754-109">Name</span></span></p></th>
<th><p><span data-ttu-id="17754-110">Obrigatório/Opcional</span><span class="sxs-lookup"><span data-stu-id="17754-110">Required/Optional</span></span></p></th>
<th><p><span data-ttu-id="17754-111">Tipo de dados</span><span class="sxs-lookup"><span data-stu-id="17754-111">Data Type</span></span></p></th>
<th><p><span data-ttu-id="17754-112">Descrição</span><span class="sxs-lookup"><span data-stu-id="17754-112">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="17754-113">Name</span><span class="sxs-lookup"><span data-stu-id="17754-113">Name</span></span></p></td>
<td><p><span data-ttu-id="17754-114">Obrigatório</span><span class="sxs-lookup"><span data-stu-id="17754-114">Required</span></span></p></td>
<td><p><span data-ttu-id="17754-115"><strong>String</strong></span><span class="sxs-lookup"><span data-stu-id="17754-115"><strong>String</strong></span></span></p></td>
<td><p><span data-ttu-id="17754-p101">A origem dos registros para o novo <strong>Recordset</strong>. A origem pode ser um nome de tabela, um nome de consulta ou uma instrução SQL que retorna registros. Para objetos de <strong>Recordset</strong> do tipo tabela nos mecanismos de banco de dados do Microsoft Access, a origem pode ser apenas um nome de tabela.  </span><span class="sxs-lookup"><span data-stu-id="17754-p101">The source of the records for the new <strong>Recordset</strong>. The source can be a table name, a query name, or an SQL statement that returns records. For table-type <strong>Recordset</strong> objects in Microsoft Access database engine databases, the source can only be a table name.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="17754-119">Tipo</span><span class="sxs-lookup"><span data-stu-id="17754-119">Type</span></span></p></td>
<td><p><span data-ttu-id="17754-120">Opcional</span><span class="sxs-lookup"><span data-stu-id="17754-120">Optional</span></span></p></td>
<td><p><span data-ttu-id="17754-121"><strong>Variant</strong></span><span class="sxs-lookup"><span data-stu-id="17754-121"><strong>Variant</strong></span></span></p></td>
<td><p><span data-ttu-id="17754-122">Uma constante <strong><a href="recordsettypeenum-enumeration-dao.md">RecordsetTypeEnum</a></strong> que indica que tipo de <strong>Recordset</strong> abrir.</span><span class="sxs-lookup"><span data-stu-id="17754-122">A <strong><a href="recordsettypeenum-enumeration-dao.md">RecordsetTypeEnum</a></strong> constant that indicates the type of <strong>Recordset</strong> to open.</span></span></p>

> [!NOTE]
> <P><span data-ttu-id="17754-p102">Se você abrir um <STRONG>Recordset</STRONG> em um espaço de trabalho do Microsoft Access se especificar um tipo, o método <STRONG>OpenRecordset</STRONG> criará um <STRONG>Recordset</STRONG> do tipo tabela, se possível. Se você especificar uma consulta ou tabela vinculada, o método <STRONG>OpenRecordset</STRONG> criará um <STRONG>Recordset</STRONG> do tipo dynaset.</span><span class="sxs-lookup"><span data-stu-id="17754-p102">If you open a <STRONG>Recordset</STRONG> in a Microsoft Access workspace and you don't specify a type, <STRONG>OpenRecordset</STRONG> creates a table-type <STRONG>Recordset</STRONG>, if possible. If you specify a linked table or query, <STRONG>OpenRecordset</STRONG> creates a dynaset-type <STRONG>Recordset</STRONG>.</span></span></P>


</td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="17754-125">Options</span><span class="sxs-lookup"><span data-stu-id="17754-125">Options</span></span></p></td>
<td><p><span data-ttu-id="17754-126">Opcional</span><span class="sxs-lookup"><span data-stu-id="17754-126">Optional</span></span></p></td>
<td><p><span data-ttu-id="17754-127"><strong>Variant</strong></span><span class="sxs-lookup"><span data-stu-id="17754-127"><strong>Variant</strong></span></span></p></td>
<td><p><span data-ttu-id="17754-128">Uma combinação de constantes <strong><a href="recordsetoptionenum-enumeration-dao.md">RecordsetOptionEnum</a></strong> que especifica as características do novo <strong>Recordset</strong>.</span><span class="sxs-lookup"><span data-stu-id="17754-128">A combination of <strong><a href="recordsetoptionenum-enumeration-dao.md">RecordsetOptionEnum</a></strong> constants that specify characteristics of the new <strong>Recordset</strong>.</span></span></p>

> [!NOTE]
> <P><span data-ttu-id="17754-129">As constantes <STRONG>dbConsistent</STRONG> e <STRONG>dbInconsistent</STRONG> são mutuamente exclusivos e usando os dois causará um erro.</span><span class="sxs-lookup"><span data-stu-id="17754-129">The constants <STRONG>dbConsistent</STRONG> and <STRONG>dbInconsistent</STRONG> are mutually exclusive, and using both causes an error.</span></span> <span data-ttu-id="17754-130">Também fornecer um argumento lockedits quando opções usa a constante <STRONG>dbReadOnly</STRONG> causará um erro.</span><span class="sxs-lookup"><span data-stu-id="17754-130">Supplying a lockedits argument when options uses the <STRONG>dbReadOnly</STRONG> constant also causes an error.</span></span></P>


</td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="17754-131">LockEdit</span><span class="sxs-lookup"><span data-stu-id="17754-131">LockEdit</span></span></p></td>
<td><p><span data-ttu-id="17754-132">Opcional</span><span class="sxs-lookup"><span data-stu-id="17754-132">Optional</span></span></p></td>
<td><p><span data-ttu-id="17754-133"><strong>Variant</strong></span><span class="sxs-lookup"><span data-stu-id="17754-133"><strong>Variant</strong></span></span></p></td>
<td><p><span data-ttu-id="17754-134">Uma constante <strong><a href="locktypeenum-enumeration-dao.md">LockTypeEnum</a></strong> que determina o bloqueio do <strong>Recordset</strong>.</span><span class="sxs-lookup"><span data-stu-id="17754-134">A <strong><a href="locktypeenum-enumeration-dao.md">LockTypeEnum</a></strong> constant that determines the locking for the <strong>Recordset</strong>.</span></span></p>

> [!NOTE]
> <P><span data-ttu-id="17754-135">Você pode usar <STRONG>dbReadOnly</STRONG> no argumento options ou o argumento lockedits, mas não ambos.</span><span class="sxs-lookup"><span data-stu-id="17754-135">You can use <STRONG>dbReadOnly</STRONG> in either the options argument or the lockedits argument, but not both.</span></span> <span data-ttu-id="17754-136">Se você usá-lo para ambos os argumentos, ocorrerá um erro em tempo de execução.</span><span class="sxs-lookup"><span data-stu-id="17754-136">If you use it for both arguments, a run-time error occurs.</span></span></P>


</td>
</tr>
</tbody>
</table>


### <a name="return-value"></a><span data-ttu-id="17754-137">Valor de Retorno</span><span class="sxs-lookup"><span data-stu-id="17754-137">Return Value</span></span>

<span data-ttu-id="17754-138">Recordset</span><span class="sxs-lookup"><span data-stu-id="17754-138">Recordset</span></span>

## <a name="remarks"></a><span data-ttu-id="17754-139">Comentários</span><span class="sxs-lookup"><span data-stu-id="17754-139">Remarks</span></span>

<span data-ttu-id="17754-p105">Normalmente, se o usuário obtém esse erro ao atualizar um registro, seu código deve atualizar o conteúdo dos campos e recuperar os valores modificados recentemente. Se o erro ocorrer ao excluir um registro, seu código poderá exibir os dados do novo registro para o usuário e uma mensagem indicando que os dados foram alterados recentemente. Nesse momento, seu código pode solicitar uma confirmação de que o usuário ainda deseja excluir o registro.</span><span class="sxs-lookup"><span data-stu-id="17754-p105">Typically, if the user gets this error while updating a record, your code should refresh the contents of the fields and retrieve the newly modified values. If the error occurs while deleting a record, your code could display the new record data to the user and a message indicating that the data has recently changed. At this point, your code can request a confirmation that the user still wants to delete the record.</span></span>

<span data-ttu-id="17754-143">Você também deverá usar a constante **dbSeeChanges** se abrir um **Recordset** em um espaço de trabalho ODBC conectado ao mecanismo de banco de dados do Microsoft Access em uma tabela do Microsoft SQL Server 6.0 (ou posterior), que tenha uma coluna IDENTITY; caso contrário, ocorrerá um erro.</span><span class="sxs-lookup"><span data-stu-id="17754-143">You should also use the **dbSeeChanges** constant if you open a **Recordset** in a Microsoft Access database engine-connected ODBC workspace against a Microsoft SQL Server 6.0 (or later) table that has an IDENTITY column, otherwise an error may result.</span></span>

<span data-ttu-id="17754-p106">Abrir mais de um **Recordset** em uma fonte de dados ODBC pode falhar porque a conexão está ocupada com uma chamada **OpenRecordset** anterior. Uma forma de contornar essa situação é preencher totalmente o **Recordset** usando o método **MoveLast** assim que o **Recordset** for aberto.</span><span class="sxs-lookup"><span data-stu-id="17754-p106">Opening more than one **Recordset** on an ODBC data source may fail because the connection is busy with a prior **OpenRecordset** call. One way around this is to fully populate the **Recordset** by using the **MoveLast** method as soon as the **Recordset** is opened.</span></span>

<span data-ttu-id="17754-146">Fechar um **Recordset** com o método **[Close](connection-close-method-dao.md)** o exclui automaticamente da coleção **Recordsets**.</span><span class="sxs-lookup"><span data-stu-id="17754-146">Closing a **Recordset** with the **[Close](connection-close-method-dao.md)** method automatically deletes it from the **Recordsets** collection.</span></span>


> [!NOTE]
> <P><span data-ttu-id="17754-147">Se a <EM>fonte</EM> refere-se a uma instrução SQL composto por uma cadeia de caracteres concatenada com um valor não inteiro e os parâmetros do sistema especificarem um caractere decimal que fora dos EUA, como uma vírgula (por exemplo, strSQL = "preço &gt; " &amp; lngPrice e lngPrice = 125,50), ocorrerá um erro ao tentar abrir o <STRONG>Recordset</STRONG>.</span><span class="sxs-lookup"><span data-stu-id="17754-147">If <EM>source</EM> refers to an SQL statement composed of a string concatenated with a non-integer value, and the system parameters specify a non-U.S. decimal character such as a comma (for example, strSQL = "PRICE &gt; " &amp; lngPrice, and lngPrice = 125,50), an error occurs when you try to open the <STRONG>Recordset</STRONG>.</span></span> <span data-ttu-id="17754-148">Isso ocorre porque durante a concatenação, o número é convertido para uma sequência utilizando o caractere decimal padrão do seu sistema, e o SQL aceita apenas caracteres decimais EUA.</span><span class="sxs-lookup"><span data-stu-id="17754-148">This is because during concatenation, the number will be converted to a string using your system's default decimal character, and SQL only accepts U.S. decimal characters.</span></span></P>


