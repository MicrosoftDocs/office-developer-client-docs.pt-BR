---
<span data-ttu-id="b9c63-101"><<<<<<< Título cabeça: propriedade IsolationLevel (ADO) TOCTitle: propriedade IsolationLevel (ADO) === título: propriedade IsolationLevel (ADO) TOCTitle: propriedade IsolationLevel (ADO)</span><span class="sxs-lookup"><span data-stu-id="b9c63-101"><<<<<<< HEAD title: IsolationLevel Property (ADO) TOCTitle: IsolationLevel Property (ADO) ======= title: IsolationLevel property (ADO) TOCTitle: IsolationLevel property (ADO)</span></span>
>>>>>>> <span data-ttu-id="b9c63-102">ms:assetid de mestre: 19461be5-c94b-4b61-ce08-7abdf702c3dc ms:mtpsurl: https://msdn.microsoft.com/library/JJ248939(v=office.15) ms:contentKeyID: ms.date 48543493: 18/09/2015 mtps_version: v=office.15</span><span class="sxs-lookup"><span data-stu-id="b9c63-102">master ms:assetid: 19461be5-c94b-4b61-ce08-7abdf702c3dc ms:mtpsurl: https://msdn.microsoft.com/library/JJ248939(v=office.15) ms:contentKeyID: 48543493 ms.date: 09/18/2015 mtps_version: v=office.15</span></span>
---

<span data-ttu-id="b9c63-103"><<<<<<< Cabeça</span><span class="sxs-lookup"><span data-stu-id="b9c63-103"><<<<<<< HEAD</span></span>
# <a name="isolationlevel-property-ado"></a><span data-ttu-id="b9c63-104">Propriedade IsolationLevel (ADO)</span><span class="sxs-lookup"><span data-stu-id="b9c63-104">IsolationLevel Property (ADO)</span></span>
=======
# <a name="isolationlevel-property-ado"></a><span data-ttu-id="b9c63-105">Propriedade IsolationLevel (ADO)</span><span class="sxs-lookup"><span data-stu-id="b9c63-105">IsolationLevel property (ADO)</span></span>
>>>>>>> <span data-ttu-id="b9c63-106">mestre</span><span class="sxs-lookup"><span data-stu-id="b9c63-106">master</span></span>


<span data-ttu-id="b9c63-107">**Aplica-se a**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="b9c63-107">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="b9c63-108">Indica o nível de isolamento de um objeto [Connection](connection-object-ado.md).</span><span class="sxs-lookup"><span data-stu-id="b9c63-108">Indicates the level of isolation for a [Connection](connection-object-ado.md) object.</span></span>

<span data-ttu-id="b9c63-109"><<<<<<< Cabeça</span><span class="sxs-lookup"><span data-stu-id="b9c63-109"><<<<<<< HEAD</span></span>
## <a name="settings-and-return-values"></a><span data-ttu-id="b9c63-110">Configurações e valor de retorno</span><span class="sxs-lookup"><span data-stu-id="b9c63-110">Settings and Return Values</span></span>
=======
## <a name="settings-and-return-values"></a><span data-ttu-id="b9c63-111">Configurações e valores de retorno</span><span class="sxs-lookup"><span data-stu-id="b9c63-111">Settings and return values</span></span>
>>>>>>> <span data-ttu-id="b9c63-112">mestre</span><span class="sxs-lookup"><span data-stu-id="b9c63-112">master</span></span>

<span data-ttu-id="b9c63-p101">Define ou retorna um valor [IsolationLevelEnum](isolationlevelenum.md). O padrão é **adXactChaos**.</span><span class="sxs-lookup"><span data-stu-id="b9c63-p101">Sets or returns an [IsolationLevelEnum](isolationlevelenum.md) value. The default is **adXactChaos**.</span></span>

## <a name="remarks"></a><span data-ttu-id="b9c63-115">Comentários</span><span class="sxs-lookup"><span data-stu-id="b9c63-115">Remarks</span></span>

<span data-ttu-id="b9c63-p102">Use a propriedade **IsolationLevel** para definir o nível de isolamento de um objeto **Connection**. A configuração só entrará em vigor na próxima vez em que você chamar o método [BeginTrans](begintrans-committrans-and-rollbacktrans-methods-ado.md). Se o nível de isolamento solicitado estiver indisponível, o provedor poderá retornar o maior nível seguinte de isolamento.</span><span class="sxs-lookup"><span data-stu-id="b9c63-p102">Use the **IsolationLevel** property to set the isolation level of a **Connection** object. The setting does not take effect until the next time you call the [BeginTrans](begintrans-committrans-and-rollbacktrans-methods-ado.md) method. If the level of isolation you request is unavailable, the provider may return the next greater level of isolation.</span></span>

<span data-ttu-id="b9c63-119">A propriedade **IsolationLevel** é leitura/gravação.</span><span class="sxs-lookup"><span data-stu-id="b9c63-119">The **IsolationLevel** property is read/write.</span></span>

<span data-ttu-id="b9c63-120">**Uso de serviço de dados remotos** Quando usado em um objeto de Conexão do cliente, a propriedade **IsolationLevel** pode ser definida somente para **adXactUnspecified**.</span><span class="sxs-lookup"><span data-stu-id="b9c63-120">**Remote Data Service Usage**When used on a client-side Connection object, the **IsolationLevel** property can be set only to **adXactUnspecified**.</span></span>

<span data-ttu-id="b9c63-p103">Como os usuários estão trabalhando com objetos **Recordset** desconectados em um cache do lado do cliente, pode haver problemas com vários usuários. Por exemplo, quando dois usuários diferentes tentam atualizar o mesmo registro, o Remote Data Service simplesmente permite que o usuário que atualizar o registro primeiro "ganhe". A solicitação de atualização do segundo usuário falhará, apresentando um erro.</span><span class="sxs-lookup"><span data-stu-id="b9c63-p103">Because users are working with disconnected **Recordset** objects on a client-side cache, there may be multiuser issues. For instance, when two different users try to update the same record, Remote Data Service simply allows the user who updates the record first to "win." The second user's update request will fail with an error.</span></span>

