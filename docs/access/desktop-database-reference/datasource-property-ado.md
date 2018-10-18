---
<span data-ttu-id="9e887-101"><<<<<<< Título cabeça: propriedade DataSource (ADO) TOCTitle: propriedade DataSource (ADO) === título: propriedade DataSource (ADO) TOCTitle: propriedade DataSource (ADO)</span><span class="sxs-lookup"><span data-stu-id="9e887-101"><<<<<<< HEAD title: DataSource Property (ADO) TOCTitle: DataSource Property (ADO) ======= title: DataSource property (ADO) TOCTitle: DataSource property (ADO)</span></span>
>>>>>>> <span data-ttu-id="9e887-102">ms:assetid de mestre: 5c5d6c9b-b7d4-45a5-0f6a-a5580a74361e ms:mtpsurl: https://msdn.microsoft.com/library/JJ249325(v=office.15) ms:contentKeyID: ms.date 48545087: 18/09/2015 mtps_version: v=office.15</span><span class="sxs-lookup"><span data-stu-id="9e887-102">master ms:assetid: 5c5d6c9b-b7d4-45a5-0f6a-a5580a74361e ms:mtpsurl: https://msdn.microsoft.com/library/JJ249325(v=office.15) ms:contentKeyID: 48545087 ms.date: 09/18/2015 mtps_version: v=office.15</span></span>
---

<span data-ttu-id="9e887-103"><<<<<<< Cabeça</span><span class="sxs-lookup"><span data-stu-id="9e887-103"><<<<<<< HEAD</span></span>
# <a name="datasource-property-ado"></a><span data-ttu-id="9e887-104">Propriedade DataSource (ADO)</span><span class="sxs-lookup"><span data-stu-id="9e887-104">DataSource Property (ADO)</span></span>
=======
# <a name="datasource-property-ado"></a><span data-ttu-id="9e887-105">Propriedade DataSource (ADO)</span><span class="sxs-lookup"><span data-stu-id="9e887-105">DataSource property (ADO)</span></span>
>>>>>>> <span data-ttu-id="9e887-106">mestre</span><span class="sxs-lookup"><span data-stu-id="9e887-106">master</span></span>


<span data-ttu-id="9e887-107">**Aplica-se a**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="9e887-107">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="9e887-108">Indica um objeto que contém dados a serem representados como um objeto [Recordset](recordset-object-ado.md).</span><span class="sxs-lookup"><span data-stu-id="9e887-108">Indicates an object that contains data to be represented as a [Recordset](recordset-object-ado.md) object.</span></span>

## <a name="remarks"></a><span data-ttu-id="9e887-109">Comentários</span><span class="sxs-lookup"><span data-stu-id="9e887-109">Remarks</span></span>

<span data-ttu-id="9e887-p101">Essa propriedade é usada para criar controles vinculados a dados no Ambiente de Dados. O Ambiente de Dados mantém as coleções de dados (fontes de dados) contendo objetos nomeados (*membros de dados*) que serão representados como um objeto \**Recordset\*\*\*.*</span><span class="sxs-lookup"><span data-stu-id="9e887-p101">This property is used to create data-bound controls with the Data Environment. The Data Environment maintains collections of data (data sources) containing named objects (*data members*) that will be represented as a **Recordset** object *.*</span></span>

<span data-ttu-id="9e887-112">As propriedades [DataMember](datamember-property-ado.md) e **DataSource** devem ser usadas em conjunto.</span><span class="sxs-lookup"><span data-stu-id="9e887-112">The [DataMember](datamember-property-ado.md) and **DataSource** properties must be used in conjunction.</span></span>

<span data-ttu-id="9e887-113">O objeto referido deve implementar a interface **IDataSource** e deve conter uma interface **IRowset**.</span><span class="sxs-lookup"><span data-stu-id="9e887-113">The object referenced must implement the **IDataSource** interface and must contain an **IRowset** interface.</span></span>

<span data-ttu-id="9e887-114">**Uso**</span><span class="sxs-lookup"><span data-stu-id="9e887-114">**Usage**</span></span>

```vb
    Dim rs as New ADODB.Recordset
    rs.DataMember = "Command"     'Name of the rowset to bind to
    Set rs.DataSource = myDE      'Name of the object containing an IRowset
```
