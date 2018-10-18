---
<span data-ttu-id="0a8b5-101"><<<<<<< Título cabeça: TOCTitle preparado Property (ADO): propriedade preparado (ADO) === título: preparado propriedade (ADO) TOCTitle: preparado propriedade (ADO)</span><span class="sxs-lookup"><span data-stu-id="0a8b5-101"><<<<<<< HEAD title: Prepared Property (ADO) TOCTitle: Prepared Property (ADO) ======= title: Prepared property (ADO) TOCTitle: Prepared property (ADO)</span></span>
>>>>>>> <span data-ttu-id="0a8b5-102">ms:assetid de mestre: 33becda2-faab-5000-8904-6ffd8c5805f2 ms:mtpsurl: https://msdn.microsoft.com/library/JJ249105(v=office.15) ms:contentKeyID: ms.date 48544116: 18/09/2015 mtps_version: v=office.15 f1_keywords:</span><span class="sxs-lookup"><span data-stu-id="0a8b5-102">master ms:assetid: 33becda2-faab-5000-8904-6ffd8c5805f2 ms:mtpsurl: https://msdn.microsoft.com/library/JJ249105(v=office.15) ms:contentKeyID: 48544116 ms.date: 09/18/2015 mtps_version: v=office.15 f1_keywords:</span></span>
- <span data-ttu-id="0a8b5-103">ado210.chm1231161 f1_categories:</span><span class="sxs-lookup"><span data-stu-id="0a8b5-103">ado210.chm1231161 f1_categories:</span></span>
- <span data-ttu-id="0a8b5-104">Office.Version=v15</span><span class="sxs-lookup"><span data-stu-id="0a8b5-104">Office.Version=v15</span></span>
---

<span data-ttu-id="0a8b5-105"><<<<<<< Cabeça</span><span class="sxs-lookup"><span data-stu-id="0a8b5-105"><<<<<<< HEAD</span></span>
# <a name="prepared-property-ado"></a><span data-ttu-id="0a8b5-106">Propriedade Prepared (ADO)</span><span class="sxs-lookup"><span data-stu-id="0a8b5-106">Prepared Property (ADO)</span></span>
=======
# <a name="prepared-property-ado"></a><span data-ttu-id="0a8b5-107">Propriedade PREPARED (ADO)</span><span class="sxs-lookup"><span data-stu-id="0a8b5-107">Prepared property (ADO)</span></span>
>>>>>>> <span data-ttu-id="0a8b5-108">mestre</span><span class="sxs-lookup"><span data-stu-id="0a8b5-108">master</span></span>


<span data-ttu-id="0a8b5-109">**Aplica-se a**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="0a8b5-109">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="0a8b5-110">Indica se uma versão compilada de um comando deve ser salva antes da execução.</span><span class="sxs-lookup"><span data-stu-id="0a8b5-110">Indicates whether to save a compiled version of a command before execution.</span></span>

<span data-ttu-id="0a8b5-111"><<<<<<< Cabeça</span><span class="sxs-lookup"><span data-stu-id="0a8b5-111"><<<<<<< HEAD</span></span>
## <a name="settings-and-return-values"></a><span data-ttu-id="0a8b5-112">Configurações e valor de retorno</span><span class="sxs-lookup"><span data-stu-id="0a8b5-112">Settings and Return Values</span></span>
=======
## <a name="settings-and-return-values"></a><span data-ttu-id="0a8b5-113">Configurações e valores de retorno</span><span class="sxs-lookup"><span data-stu-id="0a8b5-113">Settings and return values</span></span>
>>>>>>> <span data-ttu-id="0a8b5-114">mestre</span><span class="sxs-lookup"><span data-stu-id="0a8b5-114">master</span></span>

<span data-ttu-id="0a8b5-115">Define ou retorna um valor **Boolean** que, se definido como **True**, indicará que o comando deve ser preparado.</span><span class="sxs-lookup"><span data-stu-id="0a8b5-115">Sets or returns a **Boolean** value that, if set to **True**, indicates that the command should be prepared.</span></span>

## <a name="remarks"></a><span data-ttu-id="0a8b5-116">Comentários</span><span class="sxs-lookup"><span data-stu-id="0a8b5-116">Remarks</span></span>

<span data-ttu-id="0a8b5-p101">Utilize a propriedade **Prepared** para que o provedor salve uma versão preparada (ou compilada) da consulta especificada na propriedade [CommandText](commandtext-property-ado.md) antes da primeira execução de um objeto [Command](command-object-ado.md). Isto pode fazer com que a primeira execução do comando demore, mas depois que o provedor compilar um comando, ele utilizará a versão compilada do comando para quaisquer execuções subsequentes, melhorando o desempenho.</span><span class="sxs-lookup"><span data-stu-id="0a8b5-p101">Use the **Prepared** property to have the provider save a prepared (or compiled) version of the query specified in the [CommandText](commandtext-property-ado.md) property before a [Command](command-object-ado.md) object's first execution. This may slow a command's first execution, but once the provider compiles a command, the provider will use the compiled version of the command for any subsequent executions, which will result in improved performance.</span></span>

<span data-ttu-id="0a8b5-119">Se a propriedade for **False**, o provedor executará o objeto **Command** diretamente sem criar uma versão compilada.</span><span class="sxs-lookup"><span data-stu-id="0a8b5-119">If the property is **False**, the provider will execute the **Command** object directly without creating a compiled version.</span></span>

<span data-ttu-id="0a8b5-p102">Se o provedor não oferecer suporte à preparação do comando, ele poderá retornar um erro assim que essa propriedade for definida como **True**. Se não retornar um erro, ele simplesmente ignorará a solicitação para preparar o comando e definirá a propriedade **Prepared** como **False**.</span><span class="sxs-lookup"><span data-stu-id="0a8b5-p102">If the provider does not support command preparation, it may return an error as soon as this property is set to **True**. If it does not return an error, it simply ignores the request to prepare the command and sets the **Prepared** property to **False**.</span></span>

