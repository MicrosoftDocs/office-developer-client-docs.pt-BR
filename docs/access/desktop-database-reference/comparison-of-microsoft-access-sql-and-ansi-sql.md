---
title: Comparação entre Microsoft Access SQL e ANSI SQL
TOCTitle: Comparison of Microsoft Access SQL and ANSI SQL
ms:assetid: 0686f98f-10fe-0e02-e9d1-84ff3e755b57
ms:mtpsurl: https://msdn.microsoft.com/library/Ff844937(v=office.15)
ms:contentKeyID: 48543052
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: cd5350248c33b344695a02020b4b91bdbb1bb984
ms.sourcegitcommit: 38d0db57580cc5f4a0231c27b1643f8db5431ca3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/02/2018
ms.locfileid: "25937173"
---
# <a name="comparison-of-microsoft-access-sql-and-ansi-sql"></a><span data-ttu-id="98674-102">Comparação entre Microsoft Access SQL e ANSI SQL</span><span class="sxs-lookup"><span data-stu-id="98674-102">Comparison of Microsoft Access SQL and ANSI SQL</span></span>


<span data-ttu-id="98674-103">**Aplica-se a**: Access 2013, o Office 2013</span><span class="sxs-lookup"><span data-stu-id="98674-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="98674-104">O mecanismo de banco de dados Microsoft Access SQL é normalmente compatível com ANSI-89 Nível 1.</span><span class="sxs-lookup"><span data-stu-id="98674-104">Microsoft Access database engine SQL is generally ANSI-89 Level 1 compliant.</span></span> <span data-ttu-id="98674-105">No entanto, certos recursos do ANSI SQL não são implementados no Microsoft Access SQL.</span><span class="sxs-lookup"><span data-stu-id="98674-105">However, certain ANSI SQL features are not implemented in Microsoft Access SQL.</span></span> <span data-ttu-id="98674-106">Em oposição, o Microsoft Access SQL inclui palavras reservadas e recursos não aceitos no ANSI SQL.</span><span class="sxs-lookup"><span data-stu-id="98674-106">Conversely, Microsoft Access SQL includes reserved words and features not supported in ANSI SQL.</span></span>

## <a name="major-differences"></a><span data-ttu-id="98674-107">Principais diferenças</span><span class="sxs-lookup"><span data-stu-id="98674-107">Major Differences</span></span>

  - <span data-ttu-id="98674-p102">O Microsoft Access SQL e o ANSI SQL têm diferentes palavras reservadas e tipos de dados. Para obter mais informações, consulte [Palavras reservadas SQL do mecanismo de banco de dados do Microsoft Access](sql-reserved-words.md) e [Tipos de dados ANSI SQL equivalentes](equivalent-ansi-sql-data-types.md). Utilizando o Provedor do OLE DB do mecanismo de banco de dados do Microsoft Access, há outras palavras reservadas.</span><span class="sxs-lookup"><span data-stu-id="98674-p102">Microsoft Access SQL and ANSI SQL each have different reserved words and data types. For more information, see [Microsoft Access Database Engine SQL Reserved Words](sql-reserved-words.md) and [Equivalent ANSI SQL Data Types](equivalent-ansi-sql-data-types.md). Using the Microsoft Access Database Engine OLE DB Provider there are additional reserved words.</span></span>

  - <span data-ttu-id="98674-111">**[Between…And](https://msdn.microsoft.com/library/ff192436\(v=office.15\))**</span><span class="sxs-lookup"><span data-stu-id="98674-111">**[Between…And](https://msdn.microsoft.com/library/ff192436\(v=office.15\))**</span></span>
    
    <span data-ttu-id="98674-112">*expr1* \[Não\] **entre** *valor1* **e** *valor2*</span><span class="sxs-lookup"><span data-stu-id="98674-112">*expr1* \[NOT\] **Between** *value1* **And** *value2*</span></span>
    
    <span data-ttu-id="98674-113">No Microsoft Access SQL, *value1* pode ser maior que *value2*; no ANSI SQL, *value1* deve ser igual ou menor que *value2.*</span><span class="sxs-lookup"><span data-stu-id="98674-113">In Microsoft Access SQL, *value1* can be greater than *value2*; in ANSI SQL, *value1* must be equal to or less than *value2.*</span></span>

  - <span data-ttu-id="98674-p103">O Microsoft Access SQL fornece suporte a caracteres curinga do ANSI SQL e a [caracteres curinga](using-wildcard-characters-in-string-comparisons.md) específicos do mecanismo de banco de dados do Microsoft Access para serem usados com o operador **[Like](https://msdn.microsoft.com/library/ff195752\(v=office.15\))**. O uso dos caracteres curinga do ANSI e do mecanismo de banco de dados do Microsoft Access é mutuamente exclusivo. Você deve usar um conjunto ou o outro e não é possível misturá-los. Os caracteres curinga do ANSI SQL estarão disponíveis somente ao utilizar o mecanismo de banco de dados do Microsoft Access e o Provedor OLE DB do mecanismo de banco de dados do Microsoft Access. Se você tentar usar os caracteres curinga do ANSI SQL no Microsoft Access ou no DAO, eles serão interpretados como literais. O oposto é verdadeiro, ao usar o Provedor OLE DB do mecanismo de banco de dados do Microsoft Access.</span><span class="sxs-lookup"><span data-stu-id="98674-p103">Microsoft Access SQL supports both ANSI SQL wildcard characters and [wildcard characters](using-wildcard-characters-in-string-comparisons.md) that are specific to the Microsoft Access database engine to use with the **[Like](https://msdn.microsoft.com/library/ff195752\(v=office.15\))** operator. The use of the ANSI and Microsoft Access database engine wildcard characters is mutually exclusive. You must use one set or the other and cannot mix them. The ANSI SQL wildcards are only available when using the Microsoft Access database engine and the Microsoft Access Database Engine OLE DB Provider. If you try to use the ANSI SQL wildcards through Microsoft Access or DAO, then they will be interpreted as literals. The opposite is true when using the Microsoft Access Database Engine OLE DB Provider.</span></span>
    
    <table>
    <colgroup>
    <col style="width: 33%" />
    <col style="width: 33%" />
    <col style="width: 33%" />
    </colgroup>
    <thead>
    <tr class="header">
    <th><p><span data-ttu-id="98674-120">Correspondência de caracteres</span><span class="sxs-lookup"><span data-stu-id="98674-120">Matching character</span></span></p></th>
    <th><p><span data-ttu-id="98674-121">Microsoft Access SQL</span><span class="sxs-lookup"><span data-stu-id="98674-121">Microsoft Access SQL</span></span></p></th>
    <th><p><span data-ttu-id="98674-122">ANSI SQL</span><span class="sxs-lookup"><span data-stu-id="98674-122">ANSI SQL</span></span></p></th>
    </tr>
    </thead>
    <tbody>
    <tr class="odd">
    <td><p><span data-ttu-id="98674-123">Qualquer caractere simples</span><span class="sxs-lookup"><span data-stu-id="98674-123">Any single character</span></span></p></td>
    <td><p><span data-ttu-id="98674-124">?</span><span class="sxs-lookup"><span data-stu-id="98674-124"></span></span></p></td>
    <td><p><span data-ttu-id="98674-125">_ (sublinhado)</span><span class="sxs-lookup"><span data-stu-id="98674-125">_ (underscore)</span></span></p></td>
    </tr>
    <tr class="even">
    <td><p><span data-ttu-id="98674-126">Zero ou mais caracteres</span><span class="sxs-lookup"><span data-stu-id="98674-126">Zero or more characters</span></span></p></td>
    <td><p>*</p></td>
    <td><p>%</p></td>
    </tr>
    </tbody>
    </table>


  - <span data-ttu-id="98674-p104">O Microsoft Access SQL é geralmente menos restritivo. Por exemplo, ele permite agrupar e ordenar caracteres em expressões.</span><span class="sxs-lookup"><span data-stu-id="98674-p104">Microsoft Access SQL is generally less restrictive. For example, it permits grouping and ordering on expressions.</span></span>

  - <span data-ttu-id="98674-129">O Microsoft Access SQL fornece suporte a expressões mais poderosas.</span><span class="sxs-lookup"><span data-stu-id="98674-129">Microsoft Access SQL supports more powerful expressions.</span></span>

## <a name="enhanced-features-of-microsoft-access-sql"></a><span data-ttu-id="98674-130">Recursos avançados do Microsoft Access SQL</span><span class="sxs-lookup"><span data-stu-id="98674-130">Enhanced Features of Microsoft Access SQL</span></span>

<span data-ttu-id="98674-131">O Microsoft Access SQL fornece os seguintes recursos avançados:</span><span class="sxs-lookup"><span data-stu-id="98674-131">Microsoft Access SQL provides the following enhanced features:</span></span>

  - <span data-ttu-id="98674-132">A instrução [TRANSFORM](transform-statement-microsoft-access-sql.md), que fornece suporte para consultas de tabela de referência cruzada.</span><span class="sxs-lookup"><span data-stu-id="98674-132">The [TRANSFORM](transform-statement-microsoft-access-sql.md) statement, which provides support for crosstab queries.</span></span>

  - <span data-ttu-id="98674-133">[Funções agregadas](sql-aggregate-functions-sql.md) adicionais, como **StDev** e **VarP**.</span><span class="sxs-lookup"><span data-stu-id="98674-133">Additional [aggregate functions](sql-aggregate-functions-sql.md), such as **StDev** and **VarP**.</span></span>

  - <span data-ttu-id="98674-134">A declaração [PARAMETERS](parameters-declaration-microsoft-access-sql.md) para definição de consulta de parâmetro.</span><span class="sxs-lookup"><span data-stu-id="98674-134">The [PARAMETERS](parameters-declaration-microsoft-access-sql.md) declaration for defining parameter queries.</span></span>

## <a name="ansi-sql-features-not-supported-in-microsoft-access-sql"></a><span data-ttu-id="98674-135">Recursos do ANSI SQL não aceitos no Microsoft Access SQL</span><span class="sxs-lookup"><span data-stu-id="98674-135">ANSI SQL Features Not Supported in Microsoft Access SQL</span></span>

<span data-ttu-id="98674-136">O Microsoft Access SQL não fornece suporte ao seguintes recursos do ANSI SQL:</span><span class="sxs-lookup"><span data-stu-id="98674-136">Microsoft Access SQL does not support the following ANSI SQL features:</span></span>

  - <span data-ttu-id="98674-p105">Referências à função de agregação DISTINCT. Por exemplo, o Microsoft Access SQL não permite SUM(DISTINCT *nome_da_coluna*).</span><span class="sxs-lookup"><span data-stu-id="98674-p105">DISTINCT aggregate function references. For example, Microsoft Access SQL does not allow SUM(DISTINCT *columnname*).</span></span>

  - <span data-ttu-id="98674-139">A cláusula LIMIT TO *nn* ROWS usada para limitar o número de linhas retornadas por uma consulta.</span><span class="sxs-lookup"><span data-stu-id="98674-139">The LIMIT TO *nn* ROWS clause used to limit the number of rows returned by a query.</span></span> <span data-ttu-id="98674-140">Você pode usar apenas a [cláusula WHERE](https://msdn.microsoft.com/library/ff195245\(v=office.15\)) para limitar o escopo de uma consulta.</span><span class="sxs-lookup"><span data-stu-id="98674-140">You can use only the [WHERE clause](https://msdn.microsoft.com/library/ff195245\(v=office.15\)) to limit the scope of a query.</span></span>

