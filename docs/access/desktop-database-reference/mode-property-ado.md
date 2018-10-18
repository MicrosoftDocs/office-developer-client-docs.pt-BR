---
<span data-ttu-id="3dbf5-101"><<<<<<< Título cabeça: modo Property (ADO) TOCTitle: modo Property (ADO) === título: a propriedade Mode (ADO) TOCTitle: a propriedade Mode (ADO)</span><span class="sxs-lookup"><span data-stu-id="3dbf5-101"><<<<<<< HEAD title: Mode Property (ADO) TOCTitle: Mode Property (ADO) ======= title: Mode property (ADO) TOCTitle: Mode property (ADO)</span></span>
>>>>>>> <span data-ttu-id="3dbf5-102">ms:assetid de mestre: 62086f4f-8624-16c4-dae1-a17475d1864d ms:mtpsurl: https://msdn.microsoft.com/library/JJ249365(v=office.15) ms:contentKeyID: ms.date 48545227: 18/09/2015 mtps_version: v=office.15</span><span class="sxs-lookup"><span data-stu-id="3dbf5-102">master ms:assetid: 62086f4f-8624-16c4-dae1-a17475d1864d ms:mtpsurl: https://msdn.microsoft.com/library/JJ249365(v=office.15) ms:contentKeyID: 48545227 ms.date: 09/18/2015 mtps_version: v=office.15</span></span>
---

<span data-ttu-id="3dbf5-103"><<<<<<< Cabeça</span><span class="sxs-lookup"><span data-stu-id="3dbf5-103"><<<<<<< HEAD</span></span>
# <a name="mode-property-ado"></a><span data-ttu-id="3dbf5-104">Propriedade Mode (ADO)</span><span class="sxs-lookup"><span data-stu-id="3dbf5-104">Mode Property (ADO)</span></span>
=======
# <a name="mode-property-ado"></a><span data-ttu-id="3dbf5-105">Propriedade Mode (ADO)</span><span class="sxs-lookup"><span data-stu-id="3dbf5-105">Mode property (ADO)</span></span>
>>>>>>> <span data-ttu-id="3dbf5-106">mestre</span><span class="sxs-lookup"><span data-stu-id="3dbf5-106">master</span></span>


<span data-ttu-id="3dbf5-107">**Aplica-se a**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="3dbf5-107">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="3dbf5-108">Indica as permissões disponíveis para modificar os dados em um objeto [Connection](connection-object-ado.md), [Record](record-object-ado.md) ou [Stream](stream-object-ado.md).</span><span class="sxs-lookup"><span data-stu-id="3dbf5-108">Indicates the available permissions for modifying data in a [Connection](connection-object-ado.md), [Record](record-object-ado.md), or [Stream](stream-object-ado.md) object.</span></span>

<span data-ttu-id="3dbf5-109"><<<<<<< Cabeça</span><span class="sxs-lookup"><span data-stu-id="3dbf5-109"><<<<<<< HEAD</span></span>
## <a name="settings-and-return-values"></a><span data-ttu-id="3dbf5-110">Configurações e valor de retorno</span><span class="sxs-lookup"><span data-stu-id="3dbf5-110">Settings and Return Values</span></span>
=======
## <a name="settings-and-return-values"></a><span data-ttu-id="3dbf5-111">Configurações e valores de retorno</span><span class="sxs-lookup"><span data-stu-id="3dbf5-111">Settings and return values</span></span>
>>>>>>> <span data-ttu-id="3dbf5-112">mestre</span><span class="sxs-lookup"><span data-stu-id="3dbf5-112">master</span></span>

<span data-ttu-id="3dbf5-p101">Define ou retorna um valor [ConnectModeEnum](connectmodeenum.md). O valor padrão para um objeto **Connection** é **adModeUnknown**. O valor padrão para um objeto **Record** é **adModeRead**. O valor padrão para um **Stream** associado a uma fonte de base (aberta com uma URL como a fonte ou como o padrão **Stream** de um **Record**) é **adModeRead**. O valor padrão para um objeto **Stream** não associado a uma fonte de base (instanciada na memória) é **adModeUnknown**.</span><span class="sxs-lookup"><span data-stu-id="3dbf5-p101">Sets or returns a [ConnectModeEnum](connectmodeenum.md) value. The default value for a **Connection** is **adModeUnknown**. The default value for a **Record** object is **adModeRead**. The default value for a **Stream** associated with an underlying source (opened with a URL as the source, or as the default **Stream** of a **Record**) is **adModeRead**. The default value for a **Stream** not associated with an underlying source (instantiated in memory) is **adModeUnknown**.</span></span>

## <a name="remarks"></a><span data-ttu-id="3dbf5-118">Comentários</span><span class="sxs-lookup"><span data-stu-id="3dbf5-118">Remarks</span></span>

<span data-ttu-id="3dbf5-p102">Use a propriedade **Mode** para definir ou retornar as permissões de acesso em uso pelo provedor na conexão atual. Você pode definir a propriedade **Mode** apenas quando o objeto **Connection** estiver fechado.</span><span class="sxs-lookup"><span data-stu-id="3dbf5-p102">Use the **Mode** property to set or return the access permissions in use by the provider on the current connection. You can set the **Mode** property only when the **Connection** object is closed.</span></span>

<span data-ttu-id="3dbf5-p103">Para um objeto **Stream**, se o modo de acesso não for especificado, ele será herdado da fonte usada para abrir o objeto **Stream**. Por exemplo, se um **Stream** for aberto a partir de um objeto **Record**, por padrão, ele será aberto no mesmo modo que o **Record**.</span><span class="sxs-lookup"><span data-stu-id="3dbf5-p103">For a **Stream** object, if the access mode is not specified, it is inherited from the source used to open the **Stream** object. For example, if a **Stream** is opened from a **Record** object, by default it is opened in the same mode as the **Record**.</span></span>

<span data-ttu-id="3dbf5-123">Esta propriedade será leitura/gravação enquanto o objeto estiver fechado e somente leitura quando estiver aberto.</span><span class="sxs-lookup"><span data-stu-id="3dbf5-123">This property is read/write while the object is closed and read-only while the object is open.</span></span>

<span data-ttu-id="3dbf5-124">**Uso de serviço de dados remotos** Quando usado em um objeto de Conexão do cliente, a propriedade **Mode** só pode ser definida como **adModeUnknown**.</span><span class="sxs-lookup"><span data-stu-id="3dbf5-124">**Remote Data Service Usage**When used on a client-side Connection object, the **Mode** property can only be set to **adModeUnknown**.</span></span>

