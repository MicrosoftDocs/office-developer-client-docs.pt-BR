---
<span data-ttu-id="6616e-101"><<<<<<< Título cabeça: propriedade DataMember (ADO) TOCTitle: propriedade DataMember (ADO) === título: propriedade DataMember (ADO) TOCTitle: propriedade DataMember (ADO)</span><span class="sxs-lookup"><span data-stu-id="6616e-101"><<<<<<< HEAD title: DataMember Property (ADO) TOCTitle: DataMember Property (ADO) ======= title: DataMember property (ADO) TOCTitle: DataMember property (ADO)</span></span>
>>>>>>> <span data-ttu-id="6616e-102">ms:assetid de mestre: f89e1d42-7993-764b-4e8a-2f449903f792 ms:mtpsurl: https://msdn.microsoft.com/library/JJ250263(v=office.15) ms:contentKeyID: ms.date 48548787: 18/09/2015 mtps_version: v=office.15</span><span class="sxs-lookup"><span data-stu-id="6616e-102">master ms:assetid: f89e1d42-7993-764b-4e8a-2f449903f792 ms:mtpsurl: https://msdn.microsoft.com/library/JJ250263(v=office.15) ms:contentKeyID: 48548787 ms.date: 09/18/2015 mtps_version: v=office.15</span></span>
---

<span data-ttu-id="6616e-103"><<<<<<< Cabeça</span><span class="sxs-lookup"><span data-stu-id="6616e-103"><<<<<<< HEAD</span></span>
# <a name="datamember-property-ado"></a><span data-ttu-id="6616e-104">Propriedade DataMember (ADO)</span><span class="sxs-lookup"><span data-stu-id="6616e-104">DataMember Property (ADO)</span></span>
=======
# <a name="datamember-property-ado"></a><span data-ttu-id="6616e-105">Propriedade DataMember (ADO)</span><span class="sxs-lookup"><span data-stu-id="6616e-105">DataMember property (ADO)</span></span>
>>>>>>> <span data-ttu-id="6616e-106">mestre</span><span class="sxs-lookup"><span data-stu-id="6616e-106">master</span></span>

<span data-ttu-id="6616e-107">**Aplica-se a**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="6616e-107">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="6616e-108">Indica o nome do membro de dados que será recuperado do objeto referido pela propriedade [DataSource](datasource-property-ado.md).</span><span class="sxs-lookup"><span data-stu-id="6616e-108">Indicates the name of the data member that will be retrieved from the object referenced by the [DataSource](datasource-property-ado.md) property.</span></span>

<span data-ttu-id="6616e-109"><<<<<<< Cabeça</span><span class="sxs-lookup"><span data-stu-id="6616e-109"><<<<<<< HEAD</span></span>
## <a name="settings-and-return-values"></a><span data-ttu-id="6616e-110">Configurações e valor de retorno</span><span class="sxs-lookup"><span data-stu-id="6616e-110">Settings and Return Values</span></span>
=======
## <a name="settings-and-return-values"></a><span data-ttu-id="6616e-111">Configurações e valores de retorno</span><span class="sxs-lookup"><span data-stu-id="6616e-111">Settings and return values</span></span>
>>>>>>> <span data-ttu-id="6616e-112">mestre</span><span class="sxs-lookup"><span data-stu-id="6616e-112">master</span></span>

<span data-ttu-id="6616e-p101">Define ou retorna um valor **String**. O nome não diferencia maiúsculas e minúsculas.</span><span class="sxs-lookup"><span data-stu-id="6616e-p101">Sets or returns a **String** value. The name is not case sensitive.</span></span>

## <a name="remarks"></a><span data-ttu-id="6616e-115">Comentários</span><span class="sxs-lookup"><span data-stu-id="6616e-115">Remarks</span></span>

<span data-ttu-id="6616e-p102">Essa propriedade é usada para criar controles vinculados a dados no Ambiente de Dados. O Ambiente de Dados mantém as coleções de dados (fontes de dados) contendo objetos nomeados (*membros de dados*) que serão representados como um objeto [Recordset](recordset-object-ado.md)*.*</span><span class="sxs-lookup"><span data-stu-id="6616e-p102">This property is used to create data-bound controls with the Data Environment. The Data Environment maintains collections of data (data sources) containing named objects (*data members*) that will be represented as a [Recordset](recordset-object-ado.md) object *.*</span></span>

<span data-ttu-id="6616e-118">As propriedades **DataMember** e **DataSource** devem ser usadas em conjunto.</span><span class="sxs-lookup"><span data-stu-id="6616e-118">The **DataMember** and **DataSource** properties must be used in conjunction.</span></span>

<span data-ttu-id="6616e-p103">A propriedade **DataMember** determina qual objeto especificado pela propriedade **DataSource** será representado como um objeto **Recordset**. O objeto **Recordset** deve ser fechado antes que essa propriedade seja definida. Ocorrerá um erro se a propriedade **DataMember** não for definida antes da propriedade **DataSource** ou se o nome do **DataMember** não for reconhecido pelo objeto especificado na propriedade **DataSource**.</span><span class="sxs-lookup"><span data-stu-id="6616e-p103">The **DataMember** property determines which object specified by the **DataSource** property will be represented as a **Recordset** object. The **Recordset** object must be closed before this property is set. An error is generated if the **DataMember** property isn't set before the **DataSource** property, or if the **DataMember** name isn't recognized by the object specified in the **DataSource** property.</span></span>

<span data-ttu-id="6616e-122">**Uso**</span><span class="sxs-lookup"><span data-stu-id="6616e-122">**Usage**</span></span>

```vb
    Dim rs as New ADODB.Recordset
    rs.DataMember = "Command"     'Name of the rowset to bind to
    Set rs.DataSource = myDE      'Name of the object containing an IRowset
```
