---
<span data-ttu-id="9d76d-101"><<<<<<< Título cabeça: propriedade Descrição (ADO) TOCTitle: propriedade Descrição (ADO) === título: a propriedade Description (ADO) TOCTitle: a propriedade Description (ADO)</span><span class="sxs-lookup"><span data-stu-id="9d76d-101"><<<<<<< HEAD title: Description Property (ADO) TOCTitle: Description Property (ADO) ======= title: Description property (ADO) TOCTitle: Description property (ADO)</span></span>
>>>>>>> <span data-ttu-id="9d76d-102">ms:assetid de mestre: 31df5e36-641c-d213-31fc-6244e2983327 ms:mtpsurl: https://msdn.microsoft.com/library/JJ249092(v=office.15) ms:contentKeyID: ms.date 48544064: 18/09/2015 mtps_version: v=office.15</span><span class="sxs-lookup"><span data-stu-id="9d76d-102">master ms:assetid: 31df5e36-641c-d213-31fc-6244e2983327 ms:mtpsurl: https://msdn.microsoft.com/library/JJ249092(v=office.15) ms:contentKeyID: 48544064 ms.date: 09/18/2015 mtps_version: v=office.15</span></span>
---

<span data-ttu-id="9d76d-103"><<<<<<< Cabeça</span><span class="sxs-lookup"><span data-stu-id="9d76d-103"><<<<<<< HEAD</span></span>
# <a name="description-property-ado"></a><span data-ttu-id="9d76d-104">Propriedade Description (ADO)</span><span class="sxs-lookup"><span data-stu-id="9d76d-104">Description Property (ADO)</span></span>
=======
# <a name="description-property-ado"></a><span data-ttu-id="9d76d-105">Propriedade Description (ADO)</span><span class="sxs-lookup"><span data-stu-id="9d76d-105">Description property (ADO)</span></span>
>>>>>>> <span data-ttu-id="9d76d-106">mestre</span><span class="sxs-lookup"><span data-stu-id="9d76d-106">master</span></span>


<span data-ttu-id="9d76d-107">**Aplica-se a**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="9d76d-107">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="9d76d-108">Descreve um objeto [Error](error-object-ado.md).</span><span class="sxs-lookup"><span data-stu-id="9d76d-108">Describes an [Error](error-object-ado.md) object.</span></span>

<span data-ttu-id="9d76d-109"><<<<<<< Cabeça</span><span class="sxs-lookup"><span data-stu-id="9d76d-109"><<<<<<< HEAD</span></span>
## <a name="return-value"></a><span data-ttu-id="9d76d-110">Valor retornado</span><span class="sxs-lookup"><span data-stu-id="9d76d-110">Return Value</span></span>
=======
## <a name="return-value"></a><span data-ttu-id="9d76d-111">Valor de retorno</span><span class="sxs-lookup"><span data-stu-id="9d76d-111">Return value</span></span>
>>>>>>> <span data-ttu-id="9d76d-112">mestre</span><span class="sxs-lookup"><span data-stu-id="9d76d-112">master</span></span>

<span data-ttu-id="9d76d-113">Retorna um valor **String** contendo uma descrição do erro.</span><span class="sxs-lookup"><span data-stu-id="9d76d-113">Returns a **String** value that contains a description of the error.</span></span>

## <a name="remarks"></a><span data-ttu-id="9d76d-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="9d76d-114">Remarks</span></span>

<span data-ttu-id="9d76d-p101">Use a propriedade **Description** para obter uma breve descrição do erro. Exiba essa propriedade para alertar o usuário sobre um erro que você não pode ou não deseja resolver. A sequência virá do ADO ou de um provedor.</span><span class="sxs-lookup"><span data-stu-id="9d76d-p101">Use the **Description** property to obtain a short description of the error. Display this property to alert the user to an error that you cannot or do not want to handle. The string will come from either ADO or a provider.</span></span>

<span data-ttu-id="9d76d-p102">Os provedores são responsáveis por passar textos de erro específicos para o ADO. O ADO adiciona um objeto [Error](error-object-ado.md) à coleção **Errors** a cada erro de provedor ou alerta que recebe. Enumere a coleção **Errors** para rastrear os erros que são passados pelo provedor.</span><span class="sxs-lookup"><span data-stu-id="9d76d-p102">Providers are responsible for passing specific error text to ADO. ADO adds an [Error](error-object-ado.md) object to the **Errors** collection for each provider error or warning it receives. Enumerate the **Errors** collection to trace the errors that the provider passes.</span></span>

