---
<span data-ttu-id="2e7b1-101"><<<<<<< Título cabeça: propriedade DefaultDatabase (ADO) TOCTitle: propriedade DefaultDatabase (ADO) === título: a propriedade DefaultDatabase (ADO) TOCTitle: a propriedade DefaultDatabase (ADO)</span><span class="sxs-lookup"><span data-stu-id="2e7b1-101"><<<<<<< HEAD title: DefaultDatabase Property (ADO) TOCTitle: DefaultDatabase Property (ADO) ======= title: DefaultDatabase property (ADO) TOCTitle: DefaultDatabase property (ADO)</span></span>
>>>>>>> <span data-ttu-id="2e7b1-102">ms:assetid de mestre: a35c5631-f9d9-e51f-950b-e52169830d94 ms:mtpsurl: https://msdn.microsoft.com/library/JJ249757(v=office.15) ms:contentKeyID: ms.date 48546784: 18/09/2015 mtps_version: v=office.15</span><span class="sxs-lookup"><span data-stu-id="2e7b1-102">master ms:assetid: a35c5631-f9d9-e51f-950b-e52169830d94 ms:mtpsurl: https://msdn.microsoft.com/library/JJ249757(v=office.15) ms:contentKeyID: 48546784 ms.date: 09/18/2015 mtps_version: v=office.15</span></span>
---

<span data-ttu-id="2e7b1-103"><<<<<<< Cabeça</span><span class="sxs-lookup"><span data-stu-id="2e7b1-103"><<<<<<< HEAD</span></span>
# <a name="defaultdatabase-property-ado"></a><span data-ttu-id="2e7b1-104">Propriedade DefaultDatabase (ADO)</span><span class="sxs-lookup"><span data-stu-id="2e7b1-104">DefaultDatabase Property (ADO)</span></span>
=======
# <a name="defaultdatabase-property-ado"></a><span data-ttu-id="2e7b1-105">Propriedade DefaultDatabase (ADO)</span><span class="sxs-lookup"><span data-stu-id="2e7b1-105">DefaultDatabase property (ADO)</span></span>
>>>>>>> <span data-ttu-id="2e7b1-106">mestre</span><span class="sxs-lookup"><span data-stu-id="2e7b1-106">master</span></span>


<span data-ttu-id="2e7b1-107">**Aplica-se a**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="2e7b1-107">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="2e7b1-108">Indica o banco de dados padrão para um objeto [Connection](connection-object-ado.md).</span><span class="sxs-lookup"><span data-stu-id="2e7b1-108">Indicates the default database for a [Connection](connection-object-ado.md) object.</span></span>

<span data-ttu-id="2e7b1-109"><<<<<<< Cabeça</span><span class="sxs-lookup"><span data-stu-id="2e7b1-109"><<<<<<< HEAD</span></span>
## <a name="settings-and-return-values"></a><span data-ttu-id="2e7b1-110">Configurações e valor de retorno</span><span class="sxs-lookup"><span data-stu-id="2e7b1-110">Settings and Return Values</span></span>
=======
## <a name="settings-and-return-values"></a><span data-ttu-id="2e7b1-111">Configurações e valores de retorno</span><span class="sxs-lookup"><span data-stu-id="2e7b1-111">Settings and return values</span></span>
>>>>>>> <span data-ttu-id="2e7b1-112">mestre</span><span class="sxs-lookup"><span data-stu-id="2e7b1-112">master</span></span>

<span data-ttu-id="2e7b1-113">Define ou retorna um valor **String** que avalia o nome de um banco de dados disponível no provedor.</span><span class="sxs-lookup"><span data-stu-id="2e7b1-113">Sets or returns a **String** value that evaluates to the name of a database available from the provider.</span></span>

## <a name="remarks"></a><span data-ttu-id="2e7b1-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="2e7b1-114">Remarks</span></span>

<span data-ttu-id="2e7b1-115">Use a propriedade **DefaultDatabase** para definir ou retornar o nome do banco de dados padrão em um objeto **Connection** específico.</span><span class="sxs-lookup"><span data-stu-id="2e7b1-115">Use the **DefaultDatabase** property to set or return the name of the default database on a specific **Connection** object.</span></span>

<span data-ttu-id="2e7b1-p101">Se houver um banco de dados padrão, as sequências SQL poderão usar uma sintaxe não qualificada para acessar objetos no banco de dados. Para acessar objetos em um banco de dados que não seja aquele especificado na propriedade **DefaultDatabase**, é preciso qualificar os nomes dos objetos com o nome do banco de dados desejado. Na conexão, o provedor gravará as informações do banco de dados padrão na propriedade **DefaultDatabase**. Alguns provedores permitem apenas um banco de dados por conexão, caso em que não é possível alterar a propriedade **DefaultDatabase**.</span><span class="sxs-lookup"><span data-stu-id="2e7b1-p101">If there is a default database, SQL strings may use an unqualified syntax to access objects in that database. To access objects in a database other than the one specified in the **DefaultDatabase** property, you must qualify object names with the desired database name. Upon connection, the provider will write default database information to the **DefaultDatabase** property. Some providers allow only one database per connection, in which case you cannot change the **DefaultDatabase** property.</span></span>

<span data-ttu-id="2e7b1-120">Algumas fontes de dados e provedores talvez não ofereçam suporte a esse recurso e podem retornar um erro ou uma cadeia de caracteres vazia.</span><span class="sxs-lookup"><span data-stu-id="2e7b1-120">Some data sources and providers may not support this feature, and may return an error or an empty string.</span></span>

<span data-ttu-id="2e7b1-121">**Uso de serviço de dados remotos** Essa propriedade não está disponível em um objeto de **Conexão** do cliente.</span><span class="sxs-lookup"><span data-stu-id="2e7b1-121">**Remote Data Service Usage**This property is not available on a client-side **Connection** object.</span></span>

