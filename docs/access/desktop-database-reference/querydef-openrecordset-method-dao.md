---
title: Método QueryDef.OpenRecordset (DAO)
TOCTitle: OpenRecordset Method
ms:assetid: b4908c36-c156-e269-e2ad-b1fa20ec4884
ms:mtpsurl: https://msdn.microsoft.com/library/Ff822070(v=office.15)
ms:contentKeyID: 48547232
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: b3948ba2bd8eb63176483a97942984823b9f45b0
ms.sourcegitcommit: 1dd744993ecb4bed241ace874ad26edaef1778b8
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/06/2018
ms.locfileid: "25997144"
---
# <a name="querydefopenrecordset-method-dao"></a><span data-ttu-id="81416-102">Método QueryDef.OpenRecordset (DAO)</span><span class="sxs-lookup"><span data-stu-id="81416-102">QueryDef.OpenRecordset method (DAO)</span></span>

<span data-ttu-id="81416-103">**Aplica-se a**: Access 2013, o Office 2013</span><span class="sxs-lookup"><span data-stu-id="81416-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="81416-104">Cria e anexa um novo objeto **[Recordset](recordset-object-dao.md)** à coleção **Recordsets**.</span><span class="sxs-lookup"><span data-stu-id="81416-104">Creates a new **[Recordset](recordset-object-dao.md)** object and appends it to the **Recordsets** collection.</span></span>

## <a name="syntax"></a><span data-ttu-id="81416-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="81416-105">Syntax</span></span>

<span data-ttu-id="81416-106">*expressão* . OpenRecordset (***tipo***, ***Opções***, ***LockEdit***)</span><span class="sxs-lookup"><span data-stu-id="81416-106">*expression* .OpenRecordset(***Type***, ***Options***, ***LockEdit***)</span></span>

<span data-ttu-id="81416-107">*expressão* Uma variável que representa um objeto **QueryDef** .</span><span class="sxs-lookup"><span data-stu-id="81416-107">*expression* A variable that represents a **QueryDef** object.</span></span>

## <a name="parameters"></a><span data-ttu-id="81416-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="81416-108">Parameters</span></span>

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="81416-109">Nome</span><span class="sxs-lookup"><span data-stu-id="81416-109">Name</span></span></p></th>
<th><p><span data-ttu-id="81416-110">Obrigatório/opcional</span><span class="sxs-lookup"><span data-stu-id="81416-110">Required/optional</span></span></p></th>
<th><p><span data-ttu-id="81416-111">Tipo de dados</span><span class="sxs-lookup"><span data-stu-id="81416-111">Data type</span></span></p></th>
<th><p><span data-ttu-id="81416-112">Descrição</span><span class="sxs-lookup"><span data-stu-id="81416-112">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="81416-113"><em>Type</em></span><span class="sxs-lookup"><span data-stu-id="81416-113"><em>Type</em></span></span></p></td>
<td><p><span data-ttu-id="81416-114">Opcional</span><span class="sxs-lookup"><span data-stu-id="81416-114">Optional</span></span></p></td>
<td><p><span data-ttu-id="81416-115"><strong>Variant</strong></span><span class="sxs-lookup"><span data-stu-id="81416-115"><strong>Variant</strong></span></span></p></td>
<td><p><span data-ttu-id="81416-116">Uma constante <strong><a href="recordsettypeenum-enumeration-dao.md">RecordsetTypeEnum</a></strong> que indica que tipo de <strong>Recordset</strong> abrir.</span><span class="sxs-lookup"><span data-stu-id="81416-116">A <strong><a href="recordsettypeenum-enumeration-dao.md">RecordsetTypeEnum</a></strong> constant that indicates the type of <strong>Recordset</strong> to open.</span></span></p><p><span data-ttu-id="81416-117"><strong>Observação</strong>: se você abrir um <STRONG>Recordset</STRONG> em um espaço de trabalho do Microsoft Access e você não especificar um tipo, <STRONG>OpenRecordset</STRONG> cria um <STRONG>Recordset</STRONG>do tipo tabela, se possível.</span><span class="sxs-lookup"><span data-stu-id="81416-117"><strong>NOTE</strong>: If you open a <STRONG>Recordset</STRONG> in a Microsoft Access workspace and you don't specify a type, <STRONG>OpenRecordset</STRONG> creates a table-type <STRONG>Recordset</STRONG>, if possible.</span></span> <span data-ttu-id="81416-118">Se você especificar uma consulta ou tabela vinculada, <STRONG>OpenRecordset</STRONG> cria um <STRONG>Recordset</STRONG>do tipo dynaset.</span><span class="sxs-lookup"><span data-stu-id="81416-118">If you specify a linked table or query, <STRONG>OpenRecordset</STRONG> creates a dynaset-type <STRONG>Recordset</STRONG>.</span></span></p>
</td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="81416-119"><em>Options</em></span><span class="sxs-lookup"><span data-stu-id="81416-119"><em>Options</em></span></span></p></td>
<td><p><span data-ttu-id="81416-120">Opcional</span><span class="sxs-lookup"><span data-stu-id="81416-120">Optional</span></span></p></td>
<td><p><span data-ttu-id="81416-121"><strong>Variant</strong></span><span class="sxs-lookup"><span data-stu-id="81416-121"><strong>Variant</strong></span></span></p></td>
<td><p><span data-ttu-id="81416-122">Uma combinação de constantes <strong><a href="recordsetoptionenum-enumeration-dao.md">RecordsetOptionEnum</a></strong> que especifica as características do novo <strong>Recordset</strong>.</span><span class="sxs-lookup"><span data-stu-id="81416-122">A combination of <strong><a href="recordsetoptionenum-enumeration-dao.md">RecordsetOptionEnum</a></strong> constants that specify characteristics of the new <strong>Recordset</strong>.</span></span></p></p><p><span data-ttu-id="81416-123"><strong>Observação</strong>: as constantes <STRONG>dbConsistent</STRONG> e <STRONG>dbInconsistent</STRONG> são mutuamente exclusivos e usando os dois causará um erro.</span><span class="sxs-lookup"><span data-stu-id="81416-123"><strong>NOTE</strong>: The constants <STRONG>dbConsistent</STRONG> and <STRONG>dbInconsistent</STRONG> are mutually exclusive, and using both causes an error.</span></span> <span data-ttu-id="81416-124">Também fornecer um argumento lockedits quando opções usa a constante <STRONG>dbReadOnly</STRONG> causará um erro.</span><span class="sxs-lookup"><span data-stu-id="81416-124">Supplying a lockedits argument when options uses the <STRONG>dbReadOnly</STRONG> constant also causes an error.</span></span></p>
</td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="81416-125"><em>LockEdit</em></span><span class="sxs-lookup"><span data-stu-id="81416-125"><em>LockEdit</em></span></span></p></td>
<td><p><span data-ttu-id="81416-126">Opcional</span><span class="sxs-lookup"><span data-stu-id="81416-126">Optional</span></span></p></td>
<td><p><span data-ttu-id="81416-127"><strong>Variant</strong></span><span class="sxs-lookup"><span data-stu-id="81416-127"><strong>Variant</strong></span></span></p></td>
<td><p><span data-ttu-id="81416-128">Uma constante <strong><a href="locktypeenum-enumeration-dao.md">LockTypeEnum</a></strong> que determina o bloqueio do <strong>Recordset</strong>.</span><span class="sxs-lookup"><span data-stu-id="81416-128">A <strong><a href="locktypeenum-enumeration-dao.md">LockTypeEnum</a></strong> constant that determines the locking for the <strong>Recordset</strong>.</span></span></p></p><p><span data-ttu-id="81416-129"><strong>Observação</strong>: você pode usar <STRONG>dbReadOnly</STRONG> no argumento options ou o argumento lockedits, mas não ambos.</span><span class="sxs-lookup"><span data-stu-id="81416-129"><strong>NOTE</strong>: You can use <STRONG>dbReadOnly</STRONG> in either the options argument or the lockedits argument, but not both.</span></span> <span data-ttu-id="81416-130">Se você usá-lo para ambos os argumentos, ocorrerá um erro em tempo de execução.</span><span class="sxs-lookup"><span data-stu-id="81416-130">If you use it for both arguments, a run-time error occurs.</span></span></p>
</td>
</tr>
</tbody>
</table>


## <a name="return-value"></a><span data-ttu-id="81416-131">Valor de retorno</span><span class="sxs-lookup"><span data-stu-id="81416-131">Return value</span></span>

<span data-ttu-id="81416-132">Recordset</span><span class="sxs-lookup"><span data-stu-id="81416-132">Recordset</span></span>

## <a name="remarks"></a><span data-ttu-id="81416-133">Comentários</span><span class="sxs-lookup"><span data-stu-id="81416-133">Remarks</span></span>

<span data-ttu-id="81416-134">Você também deverá usar a constante **[dbSeeChanges](recordsetoptionenum-enumeration-dao.md)** se abrir um **Recordset** em um espaço de trabalho ODBC conectado ao mecanismo de banco de dados do Microsoft Access em uma tabela do Microsoft SQL Server 6.0 (ou posterior), que tenha uma coluna IDENTITY; caso contrário, ocorrerá um erro.</span><span class="sxs-lookup"><span data-stu-id="81416-134">You should also use the **[dbSeeChanges](recordsetoptionenum-enumeration-dao.md)** constant if you open a **Recordset** in a Microsoft Access database engine-connected ODBC workspace against a Microsoft SQL Server 6.0 (or later) table that has an IDENTITY column, otherwise an error may result.</span></span>

<span data-ttu-id="81416-p104">Abrir mais de um **Recordset** em uma fonte de dados ODBC pode falhar porque a conexão está ocupada com uma chamada **OpenRecordset** anterior. Uma forma de contornar essa situação é preencher totalmente o **Recordset** usando o método **[MoveLast](recordset-movelast-method-dao.md)** assim que o **Recordset** for aberto.</span><span class="sxs-lookup"><span data-stu-id="81416-p104">Opening more than one **Recordset** on an ODBC data source may fail because the connection is busy with a prior **OpenRecordset** call. One way around this is to fully populate the **Recordset** by using the **[MoveLast](recordset-movelast-method-dao.md)** method as soon as the **Recordset** is opened.</span></span>

<span data-ttu-id="81416-137">Fechar um **Recordset** com o método **Close** o exclui automaticamente da coleção **Recordsets**.</span><span class="sxs-lookup"><span data-stu-id="81416-137">Closing a **Recordset** with the **Close** method automatically deletes it from the **Recordsets** collection.</span></span>

> [!NOTE]
> <span data-ttu-id="81416-138">Se a *fonte* refere-se a uma instrução SQL composto por uma cadeia de caracteres concatenada com um valor não inteiro e os parâmetros do sistema especificarem um caractere decimal que fora dos EUA, como uma vírgula (por exemplo, strSQL = "preço &gt; " &amp; lngPrice e lngPrice = 125,50), ocorrerá um erro ao tentar abrir o **Recordset**.</span><span class="sxs-lookup"><span data-stu-id="81416-138">If *source* refers to an SQL statement composed of a string concatenated with a non-integer value, and the system parameters specify a non-U.S. decimal character such as a comma (for example, strSQL = "PRICE &gt; " &amp; lngPrice, and lngPrice = 125,50), an error occurs when you try to open the **Recordset**.</span></span> <span data-ttu-id="81416-139">Isso ocorre porque durante a concatenação, o número é convertido para uma sequência utilizando o caractere decimal padrão do seu sistema, e o SQL aceita apenas caracteres decimais EUA.</span><span class="sxs-lookup"><span data-stu-id="81416-139">This is because during concatenation, the number will be converted to a string using your system's default decimal character, and SQL only accepts U.S. decimal characters.</span></span>


