---
<span data-ttu-id="019d1-101"><<<<<<< Título cabeça: propriedade Direction (ADO) TOCTitle: propriedade Direction (ADO) === título: propriedade Direction (ADO) TOCTitle: a propriedade Direction (ADO)</span><span class="sxs-lookup"><span data-stu-id="019d1-101"><<<<<<< HEAD title: Direction Property (ADO) TOCTitle: Direction Property (ADO) ======= title: Direction property (ADO) TOCTitle: Direction property (ADO)</span></span>
>>>>>>> <span data-ttu-id="019d1-102">ms:assetid de mestre: 51a94abb-7ce9-9adb-2b76-5391eb9f6863 ms:mtpsurl: https://msdn.microsoft.com/library/JJ249262(v=office.15) ms:contentKeyID: ms.date 48544823: 18/09/2015 mtps_version: v=office.15</span><span class="sxs-lookup"><span data-stu-id="019d1-102">master ms:assetid: 51a94abb-7ce9-9adb-2b76-5391eb9f6863 ms:mtpsurl: https://msdn.microsoft.com/library/JJ249262(v=office.15) ms:contentKeyID: 48544823 ms.date: 09/18/2015 mtps_version: v=office.15</span></span>
---

<span data-ttu-id="019d1-103"><<<<<<< Cabeça</span><span class="sxs-lookup"><span data-stu-id="019d1-103"><<<<<<< HEAD</span></span>
# <a name="direction-property-ado"></a><span data-ttu-id="019d1-104">Propriedade Direction (ADO)</span><span class="sxs-lookup"><span data-stu-id="019d1-104">Direction Property (ADO)</span></span>
=======
# <a name="direction-property-ado"></a><span data-ttu-id="019d1-105">Propriedade Direction (ADO)</span><span class="sxs-lookup"><span data-stu-id="019d1-105">Direction property (ADO)</span></span>
>>>>>>> <span data-ttu-id="019d1-106">mestre</span><span class="sxs-lookup"><span data-stu-id="019d1-106">master</span></span>


<span data-ttu-id="019d1-107">**Aplica-se a**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="019d1-107">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="019d1-108">Indica se o [Parameter](parameter-object-ado.md) representa um parâmetro de entrada, um parâmetro de saída, um parâmetro de entrada e saída ou se o parâmetro é o valor de retorno de um procedimento armazenado.</span><span class="sxs-lookup"><span data-stu-id="019d1-108">Indicates whether the [Parameter](parameter-object-ado.md) represents an input parameter, an output parameter, an input and an output parameter, or if the parameter is the return value from a stored procedure.</span></span>

<span data-ttu-id="019d1-109"><<<<<<< Cabeça</span><span class="sxs-lookup"><span data-stu-id="019d1-109"><<<<<<< HEAD</span></span>
## <a name="settings-and-return-values"></a><span data-ttu-id="019d1-110">Configurações e valor de retorno</span><span class="sxs-lookup"><span data-stu-id="019d1-110">Settings and Return Values</span></span>
=======
## <a name="settings-and-return-values"></a><span data-ttu-id="019d1-111">Configurações e valores de retorno</span><span class="sxs-lookup"><span data-stu-id="019d1-111">Settings and return values</span></span>
>>>>>>> <span data-ttu-id="019d1-112">mestre</span><span class="sxs-lookup"><span data-stu-id="019d1-112">master</span></span>

<span data-ttu-id="019d1-113">Define ou retorna um valor [ParameterDirectionEnum](parameterdirectionenum.md).</span><span class="sxs-lookup"><span data-stu-id="019d1-113">Sets or returns a [ParameterDirectionEnum](parameterdirectionenum.md) value.</span></span>

## <a name="remarks"></a><span data-ttu-id="019d1-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="019d1-114">Remarks</span></span>

<span data-ttu-id="019d1-p101">Use a propriedade **Direction** para especificar como um parâmetro é passado de ou para um procedimento. A propriedade **Direction** é leitura/gravação; isso permite trabalhar com provedores que não retornam essa informação ou definir essa informação quando não se deseja mais que o ADO faça uma chamada extra para o provedor a fim de recuperar informações de parâmetro.</span><span class="sxs-lookup"><span data-stu-id="019d1-p101">Use the **Direction** property to specify how a parameter is passed to or from a procedure. The **Direction** property is read/write; this allows you to work with providers that don't return this information or to set this information when you don't want ADO to make an extra call to the provider to retrieve parameter information.</span></span>

<span data-ttu-id="019d1-p102">Nem todos os provedores podem determinar a direção dos parâmetros em seus procedimentos armazenados. Nesses casos, você deve definir a propriedade **Direction** antes de executar a consulta.</span><span class="sxs-lookup"><span data-stu-id="019d1-p102">Not all providers can determine the direction of parameters in their stored procedures. In these cases, you must set the **Direction** property before you execute the query.</span></span>

