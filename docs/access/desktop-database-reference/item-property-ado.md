---
<span data-ttu-id="2d00b-101"><<<<<<< Título cabeça: TOCTitle de propriedade de Item (ADO): propriedade de Item (ADO) === título: propriedade (ADO) Item TOCTitle: Item propriedade (ADO)</span><span class="sxs-lookup"><span data-stu-id="2d00b-101"><<<<<<< HEAD title: Item Property (ADO) TOCTitle: Item Property (ADO) ======= title: Item property (ADO) TOCTitle: Item property (ADO)</span></span>
>>>>>>> <span data-ttu-id="2d00b-102">ms:assetid de mestre: 793c305f-0e5b-a529-e21f-b7ab0843ed49 ms:mtpsurl: https://msdn.microsoft.com/library/JJ249499(v=office.15) ms:contentKeyID: ms.date 48545767: 18/09/2015 mtps_version: v=office.15</span><span class="sxs-lookup"><span data-stu-id="2d00b-102">master ms:assetid: 793c305f-0e5b-a529-e21f-b7ab0843ed49 ms:mtpsurl: https://msdn.microsoft.com/library/JJ249499(v=office.15) ms:contentKeyID: 48545767 ms.date: 09/18/2015 mtps_version: v=office.15</span></span>
---

<span data-ttu-id="2d00b-103"><<<<<<< Cabeça</span><span class="sxs-lookup"><span data-stu-id="2d00b-103"><<<<<<< HEAD</span></span>
# <a name="item-property-ado"></a><span data-ttu-id="2d00b-104">Propriedade Item (ADO)</span><span class="sxs-lookup"><span data-stu-id="2d00b-104">Item Property (ADO)</span></span>
=======
# <a name="item-property-ado"></a><span data-ttu-id="2d00b-105">Propriedade item (ADO)</span><span class="sxs-lookup"><span data-stu-id="2d00b-105">Item property (ADO)</span></span>
>>>>>>> <span data-ttu-id="2d00b-106">mestre</span><span class="sxs-lookup"><span data-stu-id="2d00b-106">master</span></span>

<span data-ttu-id="2d00b-107">**Aplica-se a**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="2d00b-107">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="2d00b-108">Indica um membro específico de uma coleção, por nome ou número ordinal.</span><span class="sxs-lookup"><span data-stu-id="2d00b-108">Indicates a specific member of a collection, by name or ordinal number.</span></span>

## <a name="syntax"></a><span data-ttu-id="2d00b-109">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="2d00b-109">Syntax</span></span>

<span data-ttu-id="2d00b-110">Definir o*objeto* = *conjunto*. Item (Index)</span><span class="sxs-lookup"><span data-stu-id="2d00b-110">Set*object* = *collection*.Item ( Index )</span></span>

<span data-ttu-id="2d00b-111"><<<<<<< Cabeça</span><span class="sxs-lookup"><span data-stu-id="2d00b-111"><<<<<<< HEAD</span></span>
## <a name="return-value"></a><span data-ttu-id="2d00b-112">Valor retornado</span><span class="sxs-lookup"><span data-stu-id="2d00b-112">Return Value</span></span>
=======
## <a name="return-value"></a><span data-ttu-id="2d00b-113">Valor de retorno</span><span class="sxs-lookup"><span data-stu-id="2d00b-113">Return value</span></span>
>>>>>>> <span data-ttu-id="2d00b-114">mestre</span><span class="sxs-lookup"><span data-stu-id="2d00b-114">master</span></span>

<span data-ttu-id="2d00b-115">Retorna uma referência de objeto.</span><span class="sxs-lookup"><span data-stu-id="2d00b-115">Returns an object reference.</span></span>

## <a name="parameters"></a><span data-ttu-id="2d00b-116">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="2d00b-116">Parameters</span></span>

- <span data-ttu-id="2d00b-117">*Index*</span><span class="sxs-lookup"><span data-stu-id="2d00b-117">*Index*</span></span>

- <span data-ttu-id="2d00b-118">Uma expressão **Variant** avaliada para o nome ou para o número ordinal de um objeto em uma coleção.</span><span class="sxs-lookup"><span data-stu-id="2d00b-118">A **Variant** expression that evaluates either to the name or to the ordinal number of an object in a collection.</span></span>

## <a name="remarks"></a><span data-ttu-id="2d00b-119">Comentários</span><span class="sxs-lookup"><span data-stu-id="2d00b-119">Remarks</span></span>

<span data-ttu-id="2d00b-120">Use a propriedade **Item** para retornar um objeto específico em uma coleção.</span><span class="sxs-lookup"><span data-stu-id="2d00b-120">Use the **Item** property to return a specific object in a collection.</span></span> <span data-ttu-id="2d00b-121">Se o **Item** não puder encontrar um objeto da coleção correspondente ao argumento de *índice* , ocorrerá um erro.</span><span class="sxs-lookup"><span data-stu-id="2d00b-121">If **Item** cannot find an object in the collection corresponding to the *Index* argument, an error occurs.</span></span> <span data-ttu-id="2d00b-122">Além disso, algumas coleções não oferecem suporte a objetos nomeados; para essas coleções, use referências de números ordinais.</span><span class="sxs-lookup"><span data-stu-id="2d00b-122">Also, some collections don't support named objects; for these collections, you must use ordinal number references.</span></span>

<span data-ttu-id="2d00b-123">A propriedade **Item** é a propriedade padrão para todas as coleções; assim, os formulários de sintaxe a seguir são intercambiáveis:</span><span class="sxs-lookup"><span data-stu-id="2d00b-123">The **Item** property is the default property for all collections; therefore, the following syntax forms are interchangeable:</span></span>

```vb
    collection.Item (Index)
    collection (Index)
```
