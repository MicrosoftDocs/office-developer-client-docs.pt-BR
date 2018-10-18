---
<span data-ttu-id="f9149-101"><<<<<<< Título cabeça: propriedade ParentURL (ADO) TOCTitle: propriedade ParentURL (ADO) === título: a propriedade ParentURL (ADO) TOCTitle: a propriedade ParentURL (ADO)</span><span class="sxs-lookup"><span data-stu-id="f9149-101"><<<<<<< HEAD title: ParentURL Property (ADO) TOCTitle: ParentURL Property (ADO) ======= title: ParentURL property (ADO) TOCTitle: ParentURL property (ADO)</span></span>
>>>>>>> <span data-ttu-id="f9149-102">ms:assetid de mestre: ec7ec476-6f9e-8486-fe02-74995975df5c ms:mtpsurl: https://msdn.microsoft.com/library/JJ250200(v=office.15) ms:contentKeyID: ms.date 48548517: 18/09/2015 mtps_version: v=office.15</span><span class="sxs-lookup"><span data-stu-id="f9149-102">master ms:assetid: ec7ec476-6f9e-8486-fe02-74995975df5c ms:mtpsurl: https://msdn.microsoft.com/library/JJ250200(v=office.15) ms:contentKeyID: 48548517 ms.date: 09/18/2015 mtps_version: v=office.15</span></span>
---

<span data-ttu-id="f9149-103"><<<<<<< Cabeça</span><span class="sxs-lookup"><span data-stu-id="f9149-103"><<<<<<< HEAD</span></span>
# <a name="parenturl-property-ado"></a><span data-ttu-id="f9149-104">Propriedade ParentURL (ADO)</span><span class="sxs-lookup"><span data-stu-id="f9149-104">ParentURL Property (ADO)</span></span>
=======
# <a name="parenturl-property-ado"></a><span data-ttu-id="f9149-105">Propriedade ParentURL (ADO)</span><span class="sxs-lookup"><span data-stu-id="f9149-105">ParentURL property (ADO)</span></span>
>>>>>>> <span data-ttu-id="f9149-106">mestre</span><span class="sxs-lookup"><span data-stu-id="f9149-106">master</span></span>

<span data-ttu-id="f9149-107">**Aplica-se a**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="f9149-107">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="f9149-108">Indica uma sequência de URL absoluta que aponta para o [Record](record-object-ado.md) pai do objeto **Record** atual.</span><span class="sxs-lookup"><span data-stu-id="f9149-108">Indicates an absolute URL string that points to the parent [Record](record-object-ado.md) of the current **Record** object.</span></span>

<span data-ttu-id="f9149-109"><<<<<<< Cabeça</span><span class="sxs-lookup"><span data-stu-id="f9149-109"><<<<<<< HEAD</span></span>
## <a name="return-value"></a><span data-ttu-id="f9149-110">Valor retornado</span><span class="sxs-lookup"><span data-stu-id="f9149-110">Return Value</span></span>
=======
## <a name="return-value"></a><span data-ttu-id="f9149-111">Valor de retorno</span><span class="sxs-lookup"><span data-stu-id="f9149-111">Return value</span></span>
>>>>>>> <span data-ttu-id="f9149-112">mestre</span><span class="sxs-lookup"><span data-stu-id="f9149-112">master</span></span>

<span data-ttu-id="f9149-113">Retorna um valor **String** que indica a URL do **Record** pai.</span><span class="sxs-lookup"><span data-stu-id="f9149-113">Returns a **String** value that indicates the URL of the parent **Record**.</span></span>

## <a name="remarks"></a><span data-ttu-id="f9149-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="f9149-114">Remarks</span></span>

<span data-ttu-id="f9149-p101">A propriedade **ParentURL** depende da origem utilizada para abrir o objeto **Record**. Por exemplo, o **Record** pode ser aberto com uma origem contendo um nome de caminho relativo de um diretório referido pela propriedade [ActiveConnection](activeconnection-property-ado.md).</span><span class="sxs-lookup"><span data-stu-id="f9149-p101">The **ParentURL** property depends upon the source used to open the **Record** object. For example, the **Record** may be opened with a source containing a relative path name of a directory referenced by the [ActiveConnection](activeconnection-property-ado.md) property.</span></span>

<span data-ttu-id="f9149-p102">Suponha que "second" seja uma pasta contida em "first". Abra o objeto **Record** da seguinte maneira:</span><span class="sxs-lookup"><span data-stu-id="f9149-p102">Suppose "second" is a folder contained under "first". Open the **Record** object with the following:</span></span>

```vb
    record.ActiveConnection = "https://first"
    record.Open "second"
```

<span data-ttu-id="f9149-119">Agora, o valor da propriedade **ParentURL** é a propriedade **ParentURL** é "https://first", igual da **ActiveConnection**.</span><span class="sxs-lookup"><span data-stu-id="f9149-119">Now, the value of the **ParentURL** property is **ParentURL** property is "https://first" , the same as **ActiveConnection**.</span></span>

<span data-ttu-id="f9149-120">A origem também pode ser uma URL absoluta, como "https://first/second".</span><span class="sxs-lookup"><span data-stu-id="f9149-120">The source may also be an absolute URL such as, "https://first/second" .</span></span> <span data-ttu-id="f9149-121">A propriedade **ParentURL** é então "https://first", o nível acima.</span><span class="sxs-lookup"><span data-stu-id="f9149-121">The **ParentURL** property is then "https://first" , the level above .</span></span> <span data-ttu-id="f9149-122">A propriedade **ParentURL** é então "https://first", o nível acima "segundo".</span><span class="sxs-lookup"><span data-stu-id="f9149-122">The **ParentURL** property is then "https://first" , the level above "second" .</span></span>

<span data-ttu-id="f9149-123">Essa propriedade poderá ser um valor nulo se:</span><span class="sxs-lookup"><span data-stu-id="f9149-123">This property may be a null value if:</span></span>

- <span data-ttu-id="f9149-124">Não houver pai para o objeto atual; por exemplo, se o objeto **Record** representar a raiz de um diretório.</span><span class="sxs-lookup"><span data-stu-id="f9149-124">There is no parent for the current object; for example, if the **Record** object represents the root of a directory.</span></span>

- <span data-ttu-id="f9149-125">O objeto **Record** representar uma entidade que não possa ser especificada com uma URL.</span><span class="sxs-lookup"><span data-stu-id="f9149-125">The **Record** object represents an entity that cannot be specified with a URL.</span></span>

<span data-ttu-id="f9149-126">Esta propriedade é somente leitura.</span><span class="sxs-lookup"><span data-stu-id="f9149-126">This property is read-only.</span></span>


> [!NOTE]
> - <span data-ttu-id="f9149-p104">[!OBSERVAçãO] Esta propriedade conta com suporte somente de provedores de origem de documento, como [Microsoft OLE DB Provider for Internet Publishing](microsoft-ole-db-provider-for-internet-publishing.md). Para obter mais informações, consulte [Registros e campos fornecidos pelo provedor](records-and-provider-supplied-fields.md).</span><span class="sxs-lookup"><span data-stu-id="f9149-p104">This property is only supported by document source providers, such as the [Microsoft OLE DB Provider for Internet Publishing](microsoft-ole-db-provider-for-internet-publishing.md). For more information, see [Records and Provider-Supplied Fields](records-and-provider-supplied-fields.md).</span></span>
> - <span data-ttu-id="f9149-129">[!OBSERVAçãO] URLs que utilizem o esquema http chamarão automaticamente o Microsoft OLE DB Provider for Internet Publishing.</span><span class="sxs-lookup"><span data-stu-id="f9149-129">URLs using the http scheme will automatically invoke the Microsoft OLE DB Provider for Internet Publishing.</span></span> <span data-ttu-id="f9149-130">Para obter mais informações, consulte [URLs absolutas e relativas](absolute-and-relative-urls.md).</span><span class="sxs-lookup"><span data-stu-id="f9149-130">For more information, see [Absolute and Relative URLs](absolute-and-relative-urls.md).</span></span> 
> - <span data-ttu-id="f9149-131">[!OBSERVAçãO] Se o registro atual contiver um registro de dados do **Recordset** de um ADO, acessar a propriedade **ParentURL** causará um erro de tempo de execução, indicando que nenhuma URL é possível.</span><span class="sxs-lookup"><span data-stu-id="f9149-131">If the current record contains a data record from an ADO **Recordset**, accessing the **ParentURL** property causes a run-time error, indicating that no URL is possible.</span></span>


