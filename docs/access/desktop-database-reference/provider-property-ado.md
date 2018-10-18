---
<span data-ttu-id="cb84d-101"><<<<<<< Título cabeça: TOCTitle provedor Property (ADO): propriedade do provedor (ADO) === título: propriedade Provider (ADO) TOCTitle: a propriedade Provider (ADO)</span><span class="sxs-lookup"><span data-stu-id="cb84d-101"><<<<<<< HEAD title: Provider Property (ADO) TOCTitle: Provider Property (ADO) ======= title: Provider property (ADO) TOCTitle: Provider property (ADO)</span></span>
>>>>>>> <span data-ttu-id="cb84d-102">ms:assetid de mestre: 1b795f51-93d7-431c-b1fe-0db95f69a56a ms:mtpsurl: https://msdn.microsoft.com/library/JJ248953(v=office.15) ms:contentKeyID: ms.date 48543543: 18/09/2015 mtps_version: v=office.15</span><span class="sxs-lookup"><span data-stu-id="cb84d-102">master ms:assetid: 1b795f51-93d7-431c-b1fe-0db95f69a56a ms:mtpsurl: https://msdn.microsoft.com/library/JJ248953(v=office.15) ms:contentKeyID: 48543543 ms.date: 09/18/2015 mtps_version: v=office.15</span></span>
---

<span data-ttu-id="cb84d-103"><<<<<<< Cabeça</span><span class="sxs-lookup"><span data-stu-id="cb84d-103"><<<<<<< HEAD</span></span>
# <a name="provider-property-ado"></a><span data-ttu-id="cb84d-104">Propriedade Provider (ADO)</span><span class="sxs-lookup"><span data-stu-id="cb84d-104">Provider Property (ADO)</span></span>
=======
# <a name="provider-property-ado"></a><span data-ttu-id="cb84d-105">Propriedade Provider (ADO)</span><span class="sxs-lookup"><span data-stu-id="cb84d-105">Provider property (ADO)</span></span>
>>>>>>> <span data-ttu-id="cb84d-106">mestre</span><span class="sxs-lookup"><span data-stu-id="cb84d-106">master</span></span>


<span data-ttu-id="cb84d-107">**Aplica-se a**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="cb84d-107">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="cb84d-108">Indica o nome do provedor de um objeto [Connection](connection-object-ado.md).</span><span class="sxs-lookup"><span data-stu-id="cb84d-108">Indicates the name of the provider for a [Connection](connection-object-ado.md) object.</span></span>

<span data-ttu-id="cb84d-109"><<<<<<< Cabeça</span><span class="sxs-lookup"><span data-stu-id="cb84d-109"><<<<<<< HEAD</span></span>
## <a name="settings-and-return-values"></a><span data-ttu-id="cb84d-110">Configurações e valor de retorno</span><span class="sxs-lookup"><span data-stu-id="cb84d-110">Settings and Return Values</span></span>
=======
## <a name="settings-and-return-values"></a><span data-ttu-id="cb84d-111">Configurações e valores de retorno</span><span class="sxs-lookup"><span data-stu-id="cb84d-111">Settings and return values</span></span>
>>>>>>> <span data-ttu-id="cb84d-112">mestre</span><span class="sxs-lookup"><span data-stu-id="cb84d-112">master</span></span>

<span data-ttu-id="cb84d-113">Define ou retorna um valor **String** que indica o nome do provedor.</span><span class="sxs-lookup"><span data-stu-id="cb84d-113">Sets or returns a **String** value that indicates the provider name.</span></span>

## <a name="remarks"></a><span data-ttu-id="cb84d-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="cb84d-114">Remarks</span></span>

<span data-ttu-id="cb84d-p101">Utilize a propriedade **Provider** para definir ou retornar o nome do provedor para uma conexão. Essa propriedade também pode ser definida pelo conteúdo da propriedade [ConnectionString](connectionstring-property-ado.md) ou pelo argumento \*ConnectionString \*  do método [Open](open-method-ado-connection.md); entretanto, a especificação de um provedor em mais de um local enquanto o método **Open** é chamado pode gerar resultados imprevisíveis. Se nenhum provedor for especificado, a propriedade assumirá o padrão de MSDASQL ([Microsoft OLE DB Provider for ODBC](microsoft-ole-db-provider-for-odbc.md)).</span><span class="sxs-lookup"><span data-stu-id="cb84d-p101">Use the **Provider** property to set or return the name of the provider for a connection. This property can also be set by the contents of the [ConnectionString](connectionstring-property-ado.md) property or the *ConnectionString* argument of the [Open](open-method-ado-connection.md) method; however, specifying a provider in more than one place while calling the **Open** method can have unpredictable results. If no provider is specified, the property will default to MSDASQL ([Microsoft OLE DB Provider for ODBC](microsoft-ole-db-provider-for-odbc.md)).</span></span>

<span data-ttu-id="cb84d-p102">A propriedade **Provider** é leitura/gravação quando a conexão estiver fechada e somente leitura quando estiver aberta. A definição será efetivada somente após a abertura do objeto **Connection** ou o acesso à coleção [Properties](properties-collection-ado.md) do objeto **Connection**. Haverá erro se a definição não for válida.</span><span class="sxs-lookup"><span data-stu-id="cb84d-p102">The **Provider** property is read/write when the connection is closed and read-only when it is open. The setting does not take effect until you either open the **Connection** object or access the [Properties](properties-collection-ado.md) collection of the **Connection** object. If the setting is not valid, an error occurs.</span></span>

