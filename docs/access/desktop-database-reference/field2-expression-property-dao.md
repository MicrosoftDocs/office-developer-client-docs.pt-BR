---
title: Propriedade Field2.Expression (DAO)
TOCTitle: Expression Property
ms:assetid: 8ae9db2c-7460-5bfc-0dc4-3f87e5ab30ff
ms:mtpsurl: https://msdn.microsoft.com/library/Ff197109(v=office.15)
ms:contentKeyID: 48546205
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 92d3cd9e9ed50503b4816cae03e2a69c790706ff
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/31/2018
ms.locfileid: "25878357"
---
# <a name="field2expression-property-dao"></a><span data-ttu-id="ff9b3-102">Propriedade Field2.Expression (DAO)</span><span class="sxs-lookup"><span data-stu-id="ff9b3-102">Field2.Expression Property (DAO)</span></span>

<span data-ttu-id="ff9b3-103">**Aplica-se a**: Access 2013, o Office 2013</span><span class="sxs-lookup"><span data-stu-id="ff9b3-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="ff9b3-104">Obtém ou define uma expressão que representa a fórmula de um campo calculado.</span><span class="sxs-lookup"><span data-stu-id="ff9b3-104">Gets or sets an expression that represents the formula for a calculated field.</span></span> <span data-ttu-id="ff9b3-105">**String** de leitura/gravação.</span><span class="sxs-lookup"><span data-stu-id="ff9b3-105">Read/write **String**.</span></span>

## <a name="version-information"></a><span data-ttu-id="ff9b3-106">Informações da versão</span><span class="sxs-lookup"><span data-stu-id="ff9b3-106">Version Information</span></span>

<span data-ttu-id="ff9b3-107">Version Added: Access 2010
</span><span class="sxs-lookup"><span data-stu-id="ff9b3-107">Version Added: Access 2010</span></span>

## <a name="syntax"></a><span data-ttu-id="ff9b3-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="ff9b3-108">Syntax</span></span>

<span data-ttu-id="ff9b3-109">*expressão* . Expressão</span><span class="sxs-lookup"><span data-stu-id="ff9b3-109">*expression* .Expression</span></span>

<span data-ttu-id="ff9b3-110">*expressão* Uma variável que representa um objeto **Field2** .</span><span class="sxs-lookup"><span data-stu-id="ff9b3-110">*expression* A variable that represents a **Field2** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="ff9b3-111">Comentários</span><span class="sxs-lookup"><span data-stu-id="ff9b3-111">Remarks</span></span>

<span data-ttu-id="ff9b3-112">No Access 2013, você pode criar campos de tabela que calculam valores.</span><span class="sxs-lookup"><span data-stu-id="ff9b3-112">In Access 2013, you can create table fields that calculate values.</span></span> <span data-ttu-id="ff9b3-113">Os cálculos podem incluir valores de campos na mesma tabela, bem como as funções internas do Access.</span><span class="sxs-lookup"><span data-stu-id="ff9b3-113">The calculations can include values from fields in the same table as well as built-in Access functions.</span></span>

<span data-ttu-id="ff9b3-114">O cálculo não pode conter campos de outras tabelas ou consultas.</span><span class="sxs-lookup"><span data-stu-id="ff9b3-114">The calculation cannot include fields from other tables or queries.</span></span>

<span data-ttu-id="ff9b3-115">Os resultados do cálculo são somente leitura.</span><span class="sxs-lookup"><span data-stu-id="ff9b3-115">The results of the calculation are read-only.</span></span>

## <a name="example"></a><span data-ttu-id="ff9b3-116">Exemplo</span><span class="sxs-lookup"><span data-stu-id="ff9b3-116">Example</span></span>

<span data-ttu-id="ff9b3-117">O exemplo a seguir mostra como criar um campo calculado.</span><span class="sxs-lookup"><span data-stu-id="ff9b3-117">The following example shows how to create a calculated field.</span></span> <span data-ttu-id="ff9b3-118">O método CreateField cria um campo denominado **FullName**.</span><span class="sxs-lookup"><span data-stu-id="ff9b3-118">The CreateField method creates a field named **FullName**.</span></span> <span data-ttu-id="ff9b3-119">A propriedade de expressão, em seguida, é definida como a expressão que calcula o valor do campo.</span><span class="sxs-lookup"><span data-stu-id="ff9b3-119">The Expression property is then set to the expression that calculates the value of the field.</span></span>

<span data-ttu-id="ff9b3-120">**Código de exemplo fornecido pela** [referência do programador do Microsoft Access 2010](https://www.amazon.com/Microsoft-Access-2010-Programmers-Reference/dp/8126528125).</span><span class="sxs-lookup"><span data-stu-id="ff9b3-120">**Sample code provided by** the [Microsoft Access 2010 Programmer’s Reference](https://www.amazon.com/Microsoft-Access-2010-Programmers-Reference/dp/8126528125).</span></span>

```vb
    Sub CreateCalculatedField()
        Dim dbs As DAO.Database
        Dim tdf As DAO.TableDef
        Dim fld As DAO.Field2
        
        ' get the database
        Set dbs = CurrentDb()
        
        ' create the table
        Set tdf = dbs.CreateTableDef("tblContactsCalcField")
        
        ' create the fields: first name, last name
        tdf.Fields.Append tdf.CreateField("FirstName", dbText, 20)
        tdf.Fields.Append tdf.CreateField("LastName", dbText, 20)
        
        ' create the calculated field: full name
        Set fld = tdf.CreateField("FullName", dbText, 50)
        fld.Expression = "[FirstName] & "" "" & [LastName]"
        tdf.Fields.Append fld
        
        ' append the table and cleanup
        dbs.TableDefs.Append tdf
        
    Cleanup:
        Set fld = Nothing
        Set tdf = Nothing
        Set dbs = Nothing
    End Sub
```

