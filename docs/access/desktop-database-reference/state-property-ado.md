---
<span data-ttu-id="c9e58-101"><<<<<<< Título cabeça: estado Property (ADO) TOCTitle: estado Property (ADO) === título: (ADO) da propriedade State TOCTitle: estado de propriedade (ADO)</span><span class="sxs-lookup"><span data-stu-id="c9e58-101"><<<<<<< HEAD title: State Property (ADO) TOCTitle: State Property (ADO) ======= title: State property (ADO) TOCTitle: State property (ADO)</span></span>
>>>>>>> <span data-ttu-id="c9e58-102">ms:assetid de mestre: ade0a50c-e2d8-23ac-4ea9-b012fedcd5db ms:mtpsurl: https://msdn.microsoft.com/library/JJ249819(v=office.15) ms:contentKeyID: ms.date 48547053: 18/09/2015 mtps_version: v=office.15 f1_keywords:</span><span class="sxs-lookup"><span data-stu-id="c9e58-102">master ms:assetid: ade0a50c-e2d8-23ac-4ea9-b012fedcd5db ms:mtpsurl: https://msdn.microsoft.com/library/JJ249819(v=office.15) ms:contentKeyID: 48547053 ms.date: 09/18/2015 mtps_version: v=office.15 f1_keywords:</span></span>
- <span data-ttu-id="c9e58-103">ado210.chm1231176 f1_categories:</span><span class="sxs-lookup"><span data-stu-id="c9e58-103">ado210.chm1231176 f1_categories:</span></span>
- <span data-ttu-id="c9e58-104">Office.Version=v15</span><span class="sxs-lookup"><span data-stu-id="c9e58-104">Office.Version=v15</span></span>
---

<span data-ttu-id="c9e58-105"><<<<<<< Cabeça</span><span class="sxs-lookup"><span data-stu-id="c9e58-105"><<<<<<< HEAD</span></span>
# <a name="state-property-ado"></a><span data-ttu-id="c9e58-106">Propriedade State (ADO)</span><span class="sxs-lookup"><span data-stu-id="c9e58-106">State Property (ADO)</span></span>
=======
# <a name="state-property-ado"></a><span data-ttu-id="c9e58-107">Propriedade State (ADO)</span><span class="sxs-lookup"><span data-stu-id="c9e58-107">State property (ADO)</span></span>
>>>>>>> <span data-ttu-id="c9e58-108">mestre</span><span class="sxs-lookup"><span data-stu-id="c9e58-108">master</span></span>


<span data-ttu-id="c9e58-109">**Aplica-se a**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="c9e58-109">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="c9e58-110">Indica todos os objetos aplicáveis, independentemente de seu estado: aberto ou fechado.</span><span class="sxs-lookup"><span data-stu-id="c9e58-110">Indicates for all applicable objects whether the state of the object is open or closed.</span></span>

<span data-ttu-id="c9e58-111">Indica todos os objetos aplicáveis que executam um método assíncrono, independentemente de seu estado atual: conexão, execução ou recuperação.</span><span class="sxs-lookup"><span data-stu-id="c9e58-111">Indicates for all applicable objects executing an asynchronous method, whether the current state of the object is connecting, executing, or retrieving.</span></span>

<span data-ttu-id="c9e58-112"><<<<<<< Cabeça</span><span class="sxs-lookup"><span data-stu-id="c9e58-112"><<<<<<< HEAD</span></span>
## <a name="return-value"></a><span data-ttu-id="c9e58-113">Valor retornado</span><span class="sxs-lookup"><span data-stu-id="c9e58-113">Return Value</span></span>
=======
## <a name="return-value"></a><span data-ttu-id="c9e58-114">Valor de retorno</span><span class="sxs-lookup"><span data-stu-id="c9e58-114">Return value</span></span>
>>>>>>> <span data-ttu-id="c9e58-115">mestre</span><span class="sxs-lookup"><span data-stu-id="c9e58-115">master</span></span>

<span data-ttu-id="c9e58-p101">Retorna um valor **Long** que pode ser um valor [ObjectStateEnum](objectstateenum.md). O valor padrão é **adStateClosed**.</span><span class="sxs-lookup"><span data-stu-id="c9e58-p101">Returns a **Long** value that can be an [ObjectStateEnum](objectstateenum.md) value. The default value is **adStateClosed**.</span></span>

## <a name="remarks"></a><span data-ttu-id="c9e58-118">Comentários</span><span class="sxs-lookup"><span data-stu-id="c9e58-118">Remarks</span></span>

<span data-ttu-id="c9e58-119">Você pode utilizar a propriedade **State** para identificar o estado atual de um determinado objeto em qualquer momento.</span><span class="sxs-lookup"><span data-stu-id="c9e58-119">You can use the **State** property to determine the current state of a given object at any time.</span></span>

<span data-ttu-id="c9e58-p102">A propriedade **State** do objeto pode ter uma combinação de valores. Por exemplo, se uma instrução estiver sendo executada, essa propriedade terá uma combinação de valores de **adStateOpen** e **adStateExecuting**.</span><span class="sxs-lookup"><span data-stu-id="c9e58-p102">The object's **State** property can have a combination of values. For example, if a statement is executing, this property will have a combined value of **adStateOpen** and **adStateExecuting**.</span></span>

<span data-ttu-id="c9e58-122">A propriedade **State** é somente leitura.</span><span class="sxs-lookup"><span data-stu-id="c9e58-122">The **State** property is read-only.</span></span>

