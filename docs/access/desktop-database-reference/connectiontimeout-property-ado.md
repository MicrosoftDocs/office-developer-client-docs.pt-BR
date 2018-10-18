---
<span data-ttu-id="a19b0-101"><<<<<<< Título cabeça: propriedade ConnectionTimeout (ADO) TOCTitle: propriedade ConnectionTimeout (ADO) === título: propriedade ConnectionTimeout (ADO) TOCTitle: propriedade ConnectionTimeout (ADO)</span><span class="sxs-lookup"><span data-stu-id="a19b0-101"><<<<<<< HEAD title: ConnectionTimeout Property (ADO) TOCTitle: ConnectionTimeout Property (ADO) ======= title: ConnectionTimeout property (ADO) TOCTitle: ConnectionTimeout property (ADO)</span></span>
>>>>>>> <span data-ttu-id="a19b0-102">ms:assetid de mestre: efc39fd8-afce-5ac0-2fff-cbb55c1a444d ms:mtpsurl: https://msdn.microsoft.com/library/JJ250218(v=office.15) ms:contentKeyID: ms.date 48548589: 18/09/2015 mtps_version: v=office.15</span><span class="sxs-lookup"><span data-stu-id="a19b0-102">master ms:assetid: efc39fd8-afce-5ac0-2fff-cbb55c1a444d ms:mtpsurl: https://msdn.microsoft.com/library/JJ250218(v=office.15) ms:contentKeyID: 48548589 ms.date: 09/18/2015 mtps_version: v=office.15</span></span>
---

<span data-ttu-id="a19b0-103"><<<<<<< Cabeça</span><span class="sxs-lookup"><span data-stu-id="a19b0-103"><<<<<<< HEAD</span></span>
# <a name="connectiontimeout-property-ado"></a><span data-ttu-id="a19b0-104">Propriedade ConnectionTimeout (ADO)</span><span class="sxs-lookup"><span data-stu-id="a19b0-104">ConnectionTimeout Property (ADO)</span></span>
=======
# <a name="connectiontimeout-property-ado"></a><span data-ttu-id="a19b0-105">Propriedade ConnectionTimeout (ADO)</span><span class="sxs-lookup"><span data-stu-id="a19b0-105">ConnectionTimeout property (ADO)</span></span>
>>>>>>> <span data-ttu-id="a19b0-106">mestre</span><span class="sxs-lookup"><span data-stu-id="a19b0-106">master</span></span>


<span data-ttu-id="a19b0-107">**Aplica-se a**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="a19b0-107">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="a19b0-108">Indica quanto tempo esperar ao estabelecer uma conexão antes de abortar a tentativa e gerar um erro.</span><span class="sxs-lookup"><span data-stu-id="a19b0-108">Indicates how long to wait while establishing a connection before terminating the attempt and generating an error.</span></span>

<span data-ttu-id="a19b0-109"><<<<<<< Cabeça</span><span class="sxs-lookup"><span data-stu-id="a19b0-109"><<<<<<< HEAD</span></span>
## <a name="settings-and-return-values"></a><span data-ttu-id="a19b0-110">Configurações e valor de retorno</span><span class="sxs-lookup"><span data-stu-id="a19b0-110">Settings and Return Values</span></span>
=======
## <a name="settings-and-return-values"></a><span data-ttu-id="a19b0-111">Configurações e valores de retorno</span><span class="sxs-lookup"><span data-stu-id="a19b0-111">Settings and return values</span></span>
>>>>>>> <span data-ttu-id="a19b0-112">mestre</span><span class="sxs-lookup"><span data-stu-id="a19b0-112">master</span></span>

<span data-ttu-id="a19b0-p101">Define ou retorna um valor **Long** que indica, em segundos, quanto tempo esperar para que a conexão seja aberta. O padrão é 15.</span><span class="sxs-lookup"><span data-stu-id="a19b0-p101">Sets or returns a **Long** value that indicates, in seconds, how long to wait for the connection to open. Default is 15.</span></span>

## <a name="remarks"></a><span data-ttu-id="a19b0-115">Comentários</span><span class="sxs-lookup"><span data-stu-id="a19b0-115">Remarks</span></span>

<span data-ttu-id="a19b0-p102">Use a propriedade **ConnectionTimeout** em um objeto [Connection](connection-object-ado.md) se os atrasos no tráfego da rede ou o uso intenso do servidor tornarem necessário o abandono da tentativa de conexão. Se o tempo de definição da propriedade **ConnectionTimeout** terminar antes da abertura da conexão, um erro será gerado e o ADO cancelará a tentativa. Se você definir a propriedade como zero, o ADO esperará indefinidamente até que conexão seja aberta. Verifique se o provedor no qual você está escrevendo o código oferece suporte à funcionalidade **ConnectionTimeout**.</span><span class="sxs-lookup"><span data-stu-id="a19b0-p102">Use the **ConnectionTimeout** property on a [Connection](connection-object-ado.md) object if delays from network traffic or heavy server use make it necessary to abandon a connection attempt. If the time from the **ConnectionTimeout** property setting elapses prior to the opening of the connection, an error occurs and ADO cancels the attempt. If you set the property to zero, ADO will wait indefinitely until the connection is opened. Make sure the provider to which you are writing code supports the **ConnectionTimeout** functionality.</span></span>

<span data-ttu-id="a19b0-120">A propriedade **ConnectionTimeout** será leitura/gravação quando a conexão estiver fechada e somente leitura quando ela estiver aberta.</span><span class="sxs-lookup"><span data-stu-id="a19b0-120">The **ConnectionTimeout** property is read/write when the connection is closed and read-only when it is open.</span></span>

