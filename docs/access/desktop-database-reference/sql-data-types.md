---
title: Tipos de dados do SQL (referência de banco de dados da área de trabalho do Access)
TOCTitle: SQL data types
ms:assetid: 4fc2dc8c-7825-8fbb-ff91-a0f39ef90115
ms:mtpsurl: https://msdn.microsoft.com/library/Ff193793(v=office.15)
ms:contentKeyID: 48544783
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- jetsql40.chm5277590
f1_categories:
- Office.Version=v15
localization_priority: Priority
ms.openlocfilehash: fb72a0090550692e7cf5028a6a58a078fc5d9d32
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: pt-BR
ms.lasthandoff: 01/17/2019
ms.locfileid: "28722197"
---
# <a name="sql-data-types"></a><span data-ttu-id="49d66-102">Tipos de dados SQL</span><span class="sxs-lookup"><span data-stu-id="49d66-102">SQL data types</span></span>

<span data-ttu-id="49d66-103">**Aplica-se a**: Access 2013, o Office 2013</span><span class="sxs-lookup"><span data-stu-id="49d66-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="49d66-104">Os tipos de dados SQL do mecanismo de banco de dados do Microsoft Access consistem em 13 tipos de dados principais definidos pelo mecanismo de banco de dados do Microsoft Jet e vários sinônimos válidos, reconhecidos para esses tipos de dados.</span><span class="sxs-lookup"><span data-stu-id="49d66-104">The Microsoft Access database engine SQL data types consist of 13 primary data types defined by the Microsoft Jet database engine and several valid synonyms recognized for these data types.</span></span>

<span data-ttu-id="49d66-p101">A tabela a seguir lista os principais tipos de dados. Os sinônimos são identificados em [Palavras reservadas SQL do mecanismo de banco de dados Microsoft Access](sql-reserved-words.md).</span><span class="sxs-lookup"><span data-stu-id="49d66-p101">The following table lists the primary data types. The synonyms are identified in [Microsoft Access Database Engine SQL Reserved Words](sql-reserved-words.md).</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="49d66-107">Tipo de dado</span><span class="sxs-lookup"><span data-stu-id="49d66-107">Data type</span></span></p></th>
<th><p><span data-ttu-id="49d66-108">Espaço de repositório</span><span class="sxs-lookup"><span data-stu-id="49d66-108">Storage size</span></span></p></th>
<th><p><span data-ttu-id="49d66-109">Descrição</span><span class="sxs-lookup"><span data-stu-id="49d66-109">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="49d66-110">BINARY</span><span class="sxs-lookup"><span data-stu-id="49d66-110">BINARY</span></span></p></td>
<td><p><span data-ttu-id="49d66-111">1 byte por caractere</span><span class="sxs-lookup"><span data-stu-id="49d66-111">1 byte per character</span></span></p></td>
<td><p><span data-ttu-id="49d66-p102">Qualquer tipo de dados pode ser armazenado em um campo desse tipo. Nenhuma conversão de dados (por exemplo, para texto) é feita. A forma como os dados são inseridos em um campo binário indica o modo como serão exibidos na saída.</span><span class="sxs-lookup"><span data-stu-id="49d66-p102">Any type of data may be stored in a field of this type. No translation of the data (for example, to text) is made. How the data is input in a binary field dictates how it will appear as output.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="49d66-115">BIT</span><span class="sxs-lookup"><span data-stu-id="49d66-115">BIT</span></span></p></td>
<td><p><span data-ttu-id="49d66-116">1 byte</span><span class="sxs-lookup"><span data-stu-id="49d66-116">1 byte</span></span></p></td>
<td><p><span data-ttu-id="49d66-117">Os valores Sim e Não e os campos que contêm apenas um desses dois valores.</span><span class="sxs-lookup"><span data-stu-id="49d66-117">Yes and No values and fields that contain only one of two values.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="49d66-118">TINYINT</span><span class="sxs-lookup"><span data-stu-id="49d66-118">TINYINT</span></span></p></td>
<td><p><span data-ttu-id="49d66-119">1 byte</span><span class="sxs-lookup"><span data-stu-id="49d66-119">1 byte</span></span></p></td>
<td><p><span data-ttu-id="49d66-120">Um valor inteiro entre 0 e 255.</span><span class="sxs-lookup"><span data-stu-id="49d66-120">An integer value between 0 and 255.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="49d66-121">MONEY</span><span class="sxs-lookup"><span data-stu-id="49d66-121">MONEY</span></span></p></td>
<td><p><span data-ttu-id="49d66-122">8 bytes</span><span class="sxs-lookup"><span data-stu-id="49d66-122">8 bytes</span></span></p></td>
<td><p><span data-ttu-id="49d66-123">Um inteiro em escala entre – 922,337,203,685,477.5808 e 922,337,203,685,477.5807.</span><span class="sxs-lookup"><span data-stu-id="49d66-123">A scaled integer between – 922,337,203,685,477.5808 and 922,337,203,685,477.5807.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="49d66-124">DATETIME (consulte DOUBLE)</span><span class="sxs-lookup"><span data-stu-id="49d66-124">DATETIME (See DOUBLE)</span></span></p></td>
<td><p><span data-ttu-id="49d66-125">8 bytes</span><span class="sxs-lookup"><span data-stu-id="49d66-125">8 bytes</span></span></p></td>
<td><p><span data-ttu-id="49d66-126">Um valor de data ou hora entre os anos 100 e 9999.</span><span class="sxs-lookup"><span data-stu-id="49d66-126">A date or time value between the years 100 and 9999.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="49d66-127">UNIQUEIDENTIFIER</span><span class="sxs-lookup"><span data-stu-id="49d66-127">UNIQUEIDENTIFIER</span></span></p></td>
<td><p><span data-ttu-id="49d66-128">128 bits</span><span class="sxs-lookup"><span data-stu-id="49d66-128">128 bits</span></span></p></td>
<td><p><span data-ttu-id="49d66-129">Um número de identificação exclusiva utilizado com as chamadas de procedimento remoto.</span><span class="sxs-lookup"><span data-stu-id="49d66-129">A unique identification number used with remote procedure calls.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="49d66-130">REAL</span><span class="sxs-lookup"><span data-stu-id="49d66-130">REAL</span></span></p></td>
<td><p><span data-ttu-id="49d66-131">4 bytes</span><span class="sxs-lookup"><span data-stu-id="49d66-131">4 bytes</span></span></p></td>
<td><p><span data-ttu-id="49d66-132">Um valor de ponto de flutuação de precisão única com um intervalo de – 3.402823E38 a – 1.401298E-45 para valores negativos, 1.401298E-45 a 3.402823E38 para valores positivos e 0.</span><span class="sxs-lookup"><span data-stu-id="49d66-132">A single-precision floating-point value with a range of – 3.402823E38 to – 1.401298E-45 for negative values, 1.401298E-45 to 3.402823E38 for positive values, and 0.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="49d66-133">FLOAT</span><span class="sxs-lookup"><span data-stu-id="49d66-133">FLOAT</span></span></p></td>
<td><p><span data-ttu-id="49d66-134">8 bytes</span><span class="sxs-lookup"><span data-stu-id="49d66-134">8 bytes</span></span></p></td>
<td><p><span data-ttu-id="49d66-135">Um valor de ponto de flutuação de precisão dupla com um intervalo de – 1.79769313486232E308 a – 4.94065645841247E-324 para valores negativos, 4.94065645841247E-324 a 1.79769313486232E308 para valores positivos e 0.</span><span class="sxs-lookup"><span data-stu-id="49d66-135">A double-precision floating-point value with a range of – 1.79769313486232E308 to – 4.94065645841247E-324 for negative values, 4.94065645841247E-324 to 1.79769313486232E308 for positive values, and 0.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="49d66-136">SMALLINT</span><span class="sxs-lookup"><span data-stu-id="49d66-136">SMALLINT</span></span></p></td>
<td><p><span data-ttu-id="49d66-137">2 bytes</span><span class="sxs-lookup"><span data-stu-id="49d66-137">2 bytes</span></span></p></td>
<td><p><span data-ttu-id="49d66-p103">Um inteiro curto entre –  32,768 e 32,767 (consulte Observações)</span><span class="sxs-lookup"><span data-stu-id="49d66-p103">A short integer between – 32,768 and 32,767. (See Notes)</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="49d66-140">INTEGER</span><span class="sxs-lookup"><span data-stu-id="49d66-140">INTEGER</span></span></p></td>
<td><p><span data-ttu-id="49d66-141">4 bytes</span><span class="sxs-lookup"><span data-stu-id="49d66-141">4 bytes</span></span></p></td>
<td><p><span data-ttu-id="49d66-p104">Um inteiro longo entre –  2,147,483,648 e 2,147,483,647 (consulte Observações)</span><span class="sxs-lookup"><span data-stu-id="49d66-p104">A long integer between – 2,147,483,648 and 2,147,483,647. (See Notes)</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="49d66-144">DECIMAL</span><span class="sxs-lookup"><span data-stu-id="49d66-144">DECIMAL</span></span></p></td>
<td><p><span data-ttu-id="49d66-145">17 bytes</span><span class="sxs-lookup"><span data-stu-id="49d66-145">17 bytes</span></span></p></td>
<td><p><span data-ttu-id="49d66-p105">Um tipo de dados numérico exato que mantém valores de 1028 - 1 a - 1028 - 1. Você pode definir a precisão (1 - 28) e a escala (0 - precisão definida). A precisão e a escala padrão são 18 e 0, respectivamente.</span><span class="sxs-lookup"><span data-stu-id="49d66-p105">An exact numeric data type that holds values from 1028 - 1 through - 1028 - 1. You can define both precision (1 - 28) and scale (0 - defined precision). The default precision and scale are 18 and 0, respectively.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="49d66-149">TEXT</span><span class="sxs-lookup"><span data-stu-id="49d66-149">TEXT</span></span></p></td>
<td><p><span data-ttu-id="49d66-150">2 bytes por caractere (Consulte Observações)</span><span class="sxs-lookup"><span data-stu-id="49d66-150">2 bytes per character (See Notes)</span></span></p></td>
<td><p><span data-ttu-id="49d66-151">Zero para um máximo de 2,14 gigabytes.</span><span class="sxs-lookup"><span data-stu-id="49d66-151">Zero to a maximum of 2.14 gigabytes.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="49d66-152">IMAGE</span><span class="sxs-lookup"><span data-stu-id="49d66-152">IMAGE</span></span></p></td>
<td><p><span data-ttu-id="49d66-153">Conforme necessário</span><span class="sxs-lookup"><span data-stu-id="49d66-153">As required</span></span></p></td>
<td><p><span data-ttu-id="49d66-p106">Zero para um máximo de 2,14 gigabytes. Usado para objetos OLE.</span><span class="sxs-lookup"><span data-stu-id="49d66-p106">Zero to a maximum of 2.14 gigabytes. Used for OLE objects.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="49d66-156">CHARACTER</span><span class="sxs-lookup"><span data-stu-id="49d66-156">CHARACTER</span></span></p></td>
<td><p><span data-ttu-id="49d66-157">2 bytes por caractere (Consulte Observações)</span><span class="sxs-lookup"><span data-stu-id="49d66-157">2 bytes per character (See Notes)</span></span></p></td>
<td><p><span data-ttu-id="49d66-158">Zero para 255 caracteres.</span><span class="sxs-lookup"><span data-stu-id="49d66-158">Zero to 255 characters.</span></span></p></td>
</tr>
</tbody>
</table>

> [!NOTE]
> - <span data-ttu-id="49d66-p107">A propagação e o incremento podem ser modificados utilizando uma [instrução ALTER TABLE](alter-table-statement-microsoft-access-sql.md). Novas linhas inseridas na tabela terão valores baseados nos novos valores de propagação e incremento, que são automaticamente gerados para a coluna. Se a nova propagação e o novo incremento puderem processar valores que correspondem a valores gerados com base na propagação e no incremento anteriores, duplicações serão geradas. Se a coluna for uma chave primária, a inserção de novas linhas poderá resultar em erros quando valores duplicados forem gerados.</span><span class="sxs-lookup"><span data-stu-id="49d66-p107">Both the seed and the increment can be modified using an [ALTER TABLE statement](alter-table-statement-microsoft-access-sql.md). New rows inserted into the table will have values, based on the new seed and increment values, that are automatically generated for the column. If the new seed and increment can yield values that match values generated based on the preceding seed and increment, duplicates will be generated. If the column is a primary key, then inserting new rows may result in errors when duplicate values are generated.</span></span>
> - <span data-ttu-id="49d66-p108">Para localizar o último valor que foi utilizado para uma coluna de incremento automático, você pode usar a seguinte instrução: SELECT @@IDENTITY. Você não pode especificar um nome de tabela. O valor retornado é da última tabela atualizada que contém uma coluna de incremento automático.</span><span class="sxs-lookup"><span data-stu-id="49d66-p108">To find the last value that was used for an auto-increment column, you can use the following statement: SELECT @@IDENTITY. You cannot specify a table name. The value returned is from the last table, containing an auto-increment column, that was updated.</span></span>
