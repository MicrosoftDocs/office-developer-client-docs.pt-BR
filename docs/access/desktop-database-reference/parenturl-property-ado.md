---
title: Propriedade ParentURL (ADO)
TOCTitle: ParentURL property (ADO)
ms:assetid: ec7ec476-6f9e-8486-fe02-74995975df5c
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250200(v=office.15)
ms:contentKeyID: 48548517
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 8e3735147f813d904c206910ff319913f056946e
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32287714"
---
# <a name="parenturl-property-ado"></a><span data-ttu-id="73bd1-102">Propriedade ParentURL (ADO)</span><span class="sxs-lookup"><span data-stu-id="73bd1-102">ParentURL property (ADO)</span></span>

<span data-ttu-id="73bd1-103">**Aplica-se ao:** Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="73bd1-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="73bd1-104">Indica uma sequência de URL absoluta que aponta para o [Record](record-object-ado.md) pai do objeto **Record** atual.</span><span class="sxs-lookup"><span data-stu-id="73bd1-104">Indicates an absolute URL string that points to the parent [Record](record-object-ado.md) of the current **Record** object.</span></span>

## <a name="return-value"></a><span data-ttu-id="73bd1-105">Valor de retorno</span><span class="sxs-lookup"><span data-stu-id="73bd1-105">Return value</span></span>

<span data-ttu-id="73bd1-106">Retorna um valor **String** que indica a URL do **Record** pai.</span><span class="sxs-lookup"><span data-stu-id="73bd1-106">Returns a **String** value that indicates the URL of the parent **Record**.</span></span>

## <a name="remarks"></a><span data-ttu-id="73bd1-107">Comentários</span><span class="sxs-lookup"><span data-stu-id="73bd1-107">Remarks</span></span>

<span data-ttu-id="73bd1-p101">A propriedade **ParentURL** depende da origem utilizada para abrir o objeto **Record**. Por exemplo, o **Record** pode ser aberto com uma origem contendo um nome de caminho relativo de um diretório referido pela propriedade [ActiveConnection](activeconnection-property-ado.md).</span><span class="sxs-lookup"><span data-stu-id="73bd1-p101">The **ParentURL** property depends upon the source used to open the **Record** object. For example, the **Record** may be opened with a source containing a relative path name of a directory referenced by the [ActiveConnection](activeconnection-property-ado.md) property.</span></span>

<span data-ttu-id="73bd1-p102">Suponha que "second" seja uma pasta contida em "first". Abra o objeto **Record** da seguinte maneira:</span><span class="sxs-lookup"><span data-stu-id="73bd1-p102">Suppose "second" is a folder contained under "first". Open the **Record** object with the following:</span></span>

```vb
    record.ActiveConnection = "https://first"
    record.Open "second"
```

<span data-ttu-id="73bd1-112">Agora, o valor da **propriedade ParentURL** é **a propriedade ParentURL** é " , o mesmo que https://first **ActiveConnection**.</span><span class="sxs-lookup"><span data-stu-id="73bd1-112">Now, the value of the **ParentURL** property is **ParentURL** property is "https://first" , the same as **ActiveConnection**.</span></span>

<span data-ttu-id="73bd1-113">A fonte também pode ser uma URL absoluta, como " https://first/second .</span><span class="sxs-lookup"><span data-stu-id="73bd1-113">The source may also be an absolute URL such as, "https://first/second" .</span></span> <span data-ttu-id="73bd1-114">A **propriedade ParentURL** é então " https://first , o nível acima .</span><span class="sxs-lookup"><span data-stu-id="73bd1-114">The **ParentURL** property is then "https://first" , the level above .</span></span> <span data-ttu-id="73bd1-115">A **propriedade ParentURL** é então " https://first " , o nível acima de "segundo" .</span><span class="sxs-lookup"><span data-stu-id="73bd1-115">The **ParentURL** property is then "https://first" , the level above "second" .</span></span>

<span data-ttu-id="73bd1-116">Essa propriedade poderá ser um valor nulo se:</span><span class="sxs-lookup"><span data-stu-id="73bd1-116">This property may be a null value if:</span></span>

- <span data-ttu-id="73bd1-117">Não houver pai para o objeto atual; por exemplo, se o objeto **Record** representar a raiz de um diretório.</span><span class="sxs-lookup"><span data-stu-id="73bd1-117">There is no parent for the current object; for example, if the **Record** object represents the root of a directory.</span></span>

- <span data-ttu-id="73bd1-118">O objeto **Record** representar uma entidade que não possa ser especificada com uma URL.</span><span class="sxs-lookup"><span data-stu-id="73bd1-118">The **Record** object represents an entity that cannot be specified with a URL.</span></span>

<span data-ttu-id="73bd1-119">Esta propriedade é somente leitura.</span><span class="sxs-lookup"><span data-stu-id="73bd1-119">This property is read-only.</span></span>


> [!NOTE]
> - <span data-ttu-id="73bd1-p104">[!OBSERVAçãO] Esta propriedade conta com suporte somente de provedores de origem de documento, como [Microsoft OLE DB Provider for Internet Publishing](microsoft-ole-db-provider-for-internet-publishing.md). Para obter mais informações, consulte [Registros e campos fornecidos pelo provedor](records-and-provider-supplied-fields.md).</span><span class="sxs-lookup"><span data-stu-id="73bd1-p104">This property is only supported by document source providers, such as the [Microsoft OLE DB Provider for Internet Publishing](microsoft-ole-db-provider-for-internet-publishing.md). For more information, see [Records and Provider-Supplied Fields](records-and-provider-supplied-fields.md).</span></span>
> - <span data-ttu-id="73bd1-122">[!OBSERVAçãO] URLs using the http scheme will automatically invoke the Microsoft OLE DB Provider for Internet Publishing.</span><span class="sxs-lookup"><span data-stu-id="73bd1-122">URLs using the http scheme will automatically invoke the Microsoft OLE DB Provider for Internet Publishing.</span></span> <span data-ttu-id="73bd1-123">Para obter mais informações, consulte [URLs absolutas e relativas](absolute-and-relative-urls.md).</span><span class="sxs-lookup"><span data-stu-id="73bd1-123">For more information, see [Absolute and Relative URLs](absolute-and-relative-urls.md).</span></span> 
> - <span data-ttu-id="73bd1-124">[!OBSERVAçãO] Se o registro atual contiver um registro de dados do **Recordset** de um ADO, acessar a propriedade **ParentURL** causará um erro de tempo de execução, indicando que nenhuma URL é possível.</span><span class="sxs-lookup"><span data-stu-id="73bd1-124">If the current record contains a data record from an ADO **Recordset**, accessing the **ParentURL** property causes a run-time error, indicating that no URL is possible.</span></span>


