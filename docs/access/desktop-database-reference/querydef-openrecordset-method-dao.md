---
title: Método QueryDef.OpenRecordset (DAO)
TOCTitle: OpenRecordset Method
ms:assetid: b4908c36-c156-e269-e2ad-b1fa20ec4884
ms:mtpsurl: https://msdn.microsoft.com/library/Ff822070(v=office.15)
ms:contentKeyID: 48547232
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Priority
ms.openlocfilehash: a046359f39611e38b9e517495f54041f876addfc
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32302846"
---
# <a name="querydefopenrecordset-method-dao"></a><span data-ttu-id="6aefa-102">Método QueryDef.OpenRecordset (DAO)</span><span class="sxs-lookup"><span data-stu-id="6aefa-102">QueryDef.OpenRecordset method (DAO)</span></span>

<span data-ttu-id="6aefa-103">**Aplica-se ao**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="6aefa-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="6aefa-104">Cria um novo objeto **[Conjunto de registros](recordset-object-dao.md)** e o acrescentar à coleção **Conjuntos de registros**.</span><span class="sxs-lookup"><span data-stu-id="6aefa-104">Creates a new **[Recordset](recordset-object-dao.md)** object and appends it to the **Recordsets** collection.</span></span>

## <a name="syntax"></a><span data-ttu-id="6aefa-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="6aefa-105">Syntax</span></span>

<span data-ttu-id="6aefa-106">*expressão* .OpenRecordset(***Tipo***, ***Opções***, ***LockEdit***)</span><span class="sxs-lookup"><span data-stu-id="6aefa-106">*expression* .OpenRecordset(***Type***, ***Options***, ***LockEdit***)</span></span>

<span data-ttu-id="6aefa-107">*expressão* uma variável que representa um objeto **QueryDef**.</span><span class="sxs-lookup"><span data-stu-id="6aefa-107">*expression*  A variable that represents a **QueryDef** object.</span></span>

## <a name="parameters"></a><span data-ttu-id="6aefa-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="6aefa-108">Parameters</span></span>

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="6aefa-109">Nome</span><span class="sxs-lookup"><span data-stu-id="6aefa-109">Name</span></span></p></th>
<th><p><span data-ttu-id="6aefa-110">Necessário/opcional</span><span class="sxs-lookup"><span data-stu-id="6aefa-110">Required/Optional</span></span></p></th>
<th><p><span data-ttu-id="6aefa-111">Tipo de dados</span><span class="sxs-lookup"><span data-stu-id="6aefa-111">Data type</span></span></p></th>
<th><p><span data-ttu-id="6aefa-112">Descrição</span><span class="sxs-lookup"><span data-stu-id="6aefa-112">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="6aefa-113"><em>Type</em></span><span class="sxs-lookup"><span data-stu-id="6aefa-113"><em>Type</em></span></span></p></td>
<td><p><span data-ttu-id="6aefa-114">Opcional</span><span class="sxs-lookup"><span data-stu-id="6aefa-114">Optional</span></span></p></td>
<td><p><span data-ttu-id="6aefa-115"><strong>Variant</strong></span><span class="sxs-lookup"><span data-stu-id="6aefa-115"><strong>Variant</strong></span></span></p></td>
<td><p><span data-ttu-id="6aefa-116">Uma constante <strong><a href="recordsettypeenum-enumeration-dao.md">RecordsetTypeEnum</a></strong> que indica que tipo de <strong>Recordset</strong> abrir.</span><span class="sxs-lookup"><span data-stu-id="6aefa-116">A <strong><a href="recordsettypeenum-enumeration-dao.md">RecordsetTypeEnum</a></strong> constant that indicates the type of <strong>Recordset</strong> to open.</span></span></p><p><span data-ttu-id="6aefa-117"><strong>OBSERVAÇÃO</strong>: Se você abrir um <STRONG>Conjunto de Registros</STRONG> em um espaço de trabalho do Microsoft Access e não especificar um tipo, o <STRONG>OpenRecordset</STRONG> criará uma tabela do tipo <STRONG>Conjunto de Registros</STRONG>, se possível.</span><span class="sxs-lookup"><span data-stu-id="6aefa-117"> > If you open a Recordset in a Microsoft Access workspace and you don't specify a type, OpenRecordset creates a table-type Recordset, if possible.</span></span> <span data-ttu-id="6aefa-118">If you specify a linked table or query, <STRONG>OpenRecordset</STRONG> creates a dynaset-type <STRONG>Recordset</STRONG>.</span><span class="sxs-lookup"><span data-stu-id="6aefa-118">If you specify a linked table or query, <STRONG>OpenRecordset</STRONG> creates a dynaset-type <STRONG>Recordset</STRONG>.</span></span></p>
</td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6aefa-119"><em>Opções</em></span><span class="sxs-lookup"><span data-stu-id="6aefa-119"><em>Options</em></span></span></p></td>
<td><p><span data-ttu-id="6aefa-120">Opcional</span><span class="sxs-lookup"><span data-stu-id="6aefa-120">Optional</span></span></p></td>
<td><p><span data-ttu-id="6aefa-121"><strong>Variant</strong></span><span class="sxs-lookup"><span data-stu-id="6aefa-121"><strong>Variant</strong></span></span></p></td>
<td><p><span data-ttu-id="6aefa-122">Uma combinação de constantes <strong><a href="recordsetoptionenum-enumeration-dao.md">RecordsetOptionEnum</a></strong> que especifica as características do novo <strong>Recordset</strong>.</span><span class="sxs-lookup"><span data-stu-id="6aefa-122">A combination of <strong><a href="recordsetoptionenum-enumeration-dao.md">RecordsetOptionEnum</a></strong> constants that specify characteristics of the new <strong>Recordset</strong>.</span></span></p></p><p><span data-ttu-id="6aefa-123"><strong>OBSERVAÇÃO</strong>: As constantes <STRONG>dbConsistent</STRONG> e <STRONG>dbInconsistent</STRONG> são mutuamente exclusivas e usar ambas causará um erro.</span><span class="sxs-lookup"><span data-stu-id="6aefa-123"> > The constants dbConsistent and dbInconsistent are mutually exclusive, and using both causes an error.</span></span> <span data-ttu-id="6aefa-124">Fornecer um argumento lockedits quando opções usa a constante <STRONG>dbReadOnly</STRONG> também causará um erro.</span><span class="sxs-lookup"><span data-stu-id="6aefa-124">Supplying a  LockEdit argument when  Options uses the dbReadOnly constant also causes an error.</span></span></p>
</td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6aefa-125"><em>LockEdit</em></span><span class="sxs-lookup"><span data-stu-id="6aefa-125"><em>LockEdit</em></span></span></p></td>
<td><p><span data-ttu-id="6aefa-126">Opcional</span><span class="sxs-lookup"><span data-stu-id="6aefa-126">Optional</span></span></p></td>
<td><p><span data-ttu-id="6aefa-127"><strong>Variant</strong></span><span class="sxs-lookup"><span data-stu-id="6aefa-127"><strong>Variant</strong></span></span></p></td>
<td><p><span data-ttu-id="6aefa-128">Uma constante <strong><a href="locktypeenum-enumeration-dao.md">LockTypeEnum</a></strong> que determina o bloqueio do <strong>Recordset</strong>.</span><span class="sxs-lookup"><span data-stu-id="6aefa-128">A <strong><a href="locktypeenum-enumeration-dao.md">LockTypeEnum</a></strong> constant that determines the locking for the <strong>Recordset</strong>.</span></span></p></p><p><span data-ttu-id="6aefa-129"><strong>OBSERVAÇÃO</strong>: você pode usar a constante <STRONG>dbReadOnly</STRONG> tanto no argumento opções quanto no lockedits, mas não em ambos.</span><span class="sxs-lookup"><span data-stu-id="6aefa-129">You can use dbReadOnly in either the Options argument or the LockedEdit argument, but not both.</span></span> <span data-ttu-id="6aefa-130">Se você usá-la para ambos argumentos, ocorrerá um erro de tempo de execução.</span><span class="sxs-lookup"><span data-stu-id="6aefa-130">If you use it for both arguments, a run-time error occurs.</span></span></p>
</td>
</tr>
</tbody>
</table>


## <a name="return-value"></a><span data-ttu-id="6aefa-131">Valor de retorno</span><span class="sxs-lookup"><span data-stu-id="6aefa-131">Return value</span></span>

<span data-ttu-id="6aefa-132">Conjunto de Registros</span><span class="sxs-lookup"><span data-stu-id="6aefa-132">Recordset</span></span>

## <a name="remarks"></a><span data-ttu-id="6aefa-133">Comentários</span><span class="sxs-lookup"><span data-stu-id="6aefa-133">Remarks</span></span>

<span data-ttu-id="6aefa-134">Você também deverá usar a constante **[dbSeeChanges](recordsetoptionenum-enumeration-dao.md)** se abrir um **Recordset** em um espaço de trabalho ODBC conectado ao mecanismo de banco de dados do Microsoft Access em uma tabela do Microsoft SQL Server 6.0 (ou posterior), que tenha uma coluna IDENTITY; caso contrário, ocorrerá um erro.</span><span class="sxs-lookup"><span data-stu-id="6aefa-134">You should also use the **[dbSeeChanges](recordsetoptionenum-enumeration-dao.md)** constant if you open a **Recordset** in a Microsoft Access database engine-connected ODBC workspace against a Microsoft SQL Server 6.0 (or later) table that has an IDENTITY column, otherwise an error may result.</span></span>

<span data-ttu-id="6aefa-p104">Abrir mais de um **Recordset** em uma fonte de dados ODBC pode falhar porque a conexão está ocupada com uma chamada **OpenRecordset** anterior. Uma forma de contornar essa situação é preencher totalmente o **Recordset** usando o método **[MoveLast](recordset-movelast-method-dao.md)** assim que o **Recordset** for aberto.</span><span class="sxs-lookup"><span data-stu-id="6aefa-p104">Opening more than one **Recordset** on an ODBC data source may fail because the connection is busy with a prior **OpenRecordset** call. One way around this is to fully populate the **Recordset** by using the **[MoveLast](recordset-movelast-method-dao.md)** method as soon as the **Recordset** is opened.</span></span>

<span data-ttu-id="6aefa-137">Fechar um **Recordset** com o método **Close** o exclui automaticamente da coleção **Recordsets**.</span><span class="sxs-lookup"><span data-stu-id="6aefa-137">Closing a **Recordset** with the **Close** method automatically deletes it from the **Recordsets** collection.</span></span>

> [!NOTE]
> <span data-ttu-id="6aefa-138">Se a *fonte* se referir a uma instrução SQL composta por uma sequência concatenada com um valor não inteiro e se os parâmetros do sistema especificarem um caractere decimal não-EUA, como uma vírgula (por exemplo, strSQL = "PRICE &gt; " &amp; lngPrice e lngPrice = 125,50), ocorrerá um erro ao tentar abrir o **Conjunto de Registros**.</span><span class="sxs-lookup"><span data-stu-id="6aefa-138">If source refers to an SQL statement composed of a string concatenated with a non-integer value, and the system parameters specify a non-U.S. decimal character such as a comma (for example, strSQL = "PRICE > " & lngPrice, and lngPrice = 125,50), an error occurs when you try to open the Recordset.</span></span> <span data-ttu-id="6aefa-139">Isso se deve ao fato de que, durante a concatenação, o número é convertido em uma cadeia de caracteres usando o caractere decimal padrão do seu sistema, e o SQL aceita apenas caracteres decimais americanos.</span><span class="sxs-lookup"><span data-stu-id="6aefa-139">This is because during concatenation, the number will be converted to a string using your system's default decimal character, and SQL only accepts U.S. decimal characters.</span></span>


