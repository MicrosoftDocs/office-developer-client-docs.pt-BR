---
title: Método CopyTo (ADO)
TOCTitle: CopyTo method (ADO)
ms:assetid: 1c1ab950-51f7-7ecc-ccd8-e689db02f06a
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248958(v=office.15)
ms:contentKeyID: 48543558
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: a17e74e1e3483b7ad2a70c5444503234cff5be12
ms.sourcegitcommit: d7248f803002b31cf7fc561b03530199a9b0a8fd
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/02/2018
ms.locfileid: "25920246"
---
# <a name="copyto-method-ado"></a><span data-ttu-id="f0a68-102">Método CopyTo (ADO)</span><span class="sxs-lookup"><span data-stu-id="f0a68-102">CopyTo method (ADO)</span></span>


<span data-ttu-id="f0a68-103">**Aplica-se a**: Access 2013, o Office 2013</span><span class="sxs-lookup"><span data-stu-id="f0a68-103">**Applies to**: Access 2013, Office 2013</span></span>


<span data-ttu-id="f0a68-104">Copia o número especificado de caracteres ou bytes (dependendo de [Type](type-property-ado-stream.md)) no [Stream](stream-object-ado.md) para outro objeto **Stream**.</span><span class="sxs-lookup"><span data-stu-id="f0a68-104">Copies the specified number of characters or bytes (depending on [Type](type-property-ado-stream.md)) in the [Stream](stream-object-ado.md) to another **Stream** object.</span></span>

## <a name="syntax"></a><span data-ttu-id="f0a68-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="f0a68-105">Syntax</span></span>

<span data-ttu-id="f0a68-106">*Stream*. CopyTo *DestStream*, *NumChars*</span><span class="sxs-lookup"><span data-stu-id="f0a68-106">*Stream*.CopyTo *DestStream*, *NumChars*</span></span>

## <a name="parameters"></a><span data-ttu-id="f0a68-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="f0a68-107">Parameters</span></span>

  - <span data-ttu-id="f0a68-108">*DestStream*</span><span class="sxs-lookup"><span data-stu-id="f0a68-108">*DestStream*</span></span>

  - <span data-ttu-id="f0a68-p101">Um valor de variável de objeto que contém uma referência para um objeto **Stream** aberto. O **Stream** atual é copiado para o **Stream** de destino especificado por *DestStream*. O **Stream** de destino já deve estar aberto. Se não estiver, ocorrerá um erro em tempo de execução.

</span><span class="sxs-lookup"><span data-stu-id="f0a68-p101">An object variable value that contains a reference to an open **Stream** object. The current **Stream** is copied to the destination **Stream** specified by *DestStream*. The destination **Stream** must already be open. If not, a run-time error occurs.</span></span>   

    > [!NOTE]
    > <span data-ttu-id="f0a68-113">O parâmetro *DestStream* não pode ser um proxy do objeto **Stream** porque isso requer acesso a uma interface particular no objeto **Stream** que não pode ser remota ao cliente.</span><span class="sxs-lookup"><span data-stu-id="f0a68-113">The *DestStream* parameter may not be a proxy of the **Stream** object because this requires access to a private interface on the **Stream** object that cannot be remoted to the client.</span></span>

  - <span data-ttu-id="f0a68-114">*NumChars*</span><span class="sxs-lookup"><span data-stu-id="f0a68-114">*NumChars*</span></span>

  - <span data-ttu-id="f0a68-115">Opcional.</span><span class="sxs-lookup"><span data-stu-id="f0a68-115">Optional.</span></span> <span data-ttu-id="f0a68-116">Um valor **Integer** que especifica o número de bytes ou caracteres a serem copiados da posição atual no **Stream** de origem para o **Stream** de destino.</span><span class="sxs-lookup"><span data-stu-id="f0a68-116">An **Integer** value that specifies the number of bytes or characters to be copied from the current position in the source **Stream** to the destination **Stream**.</span></span> <span data-ttu-id="f0a68-117">O valor padrão é -1, que especifica que todos os caracteres ou bytes são copiados na posição atual para [EOS](eos-property-ado.md).</span><span class="sxs-lookup"><span data-stu-id="f0a68-117">The default value is –1, which specifies that all characters or bytes are copied from the current position to [EOS](eos-property-ado.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="f0a68-118">Comentários</span><span class="sxs-lookup"><span data-stu-id="f0a68-118">Remarks</span></span>

<span data-ttu-id="f0a68-119">Este método copia o número especificado de caracteres ou bytes, iniciando na posição atual especificada pela propriedade [Position](position-property-ado.md).</span><span class="sxs-lookup"><span data-stu-id="f0a68-119">This method copies the specified number of characters or bytes, starting from the current position specified by the [Position](position-property-ado.md) property.</span></span> <span data-ttu-id="f0a68-120">Se o número especificado for maior que o número de bytes disponíveis até o **EOS**, apenas os caracteres ou bytes a partir da posição atual até o **EOS** serão copiados.</span><span class="sxs-lookup"><span data-stu-id="f0a68-120">If the specified number is more than the available number of bytes until **EOS**, then only characters or bytes from the current position to **EOS** are copied.</span></span> <span data-ttu-id="f0a68-121">Se o valor da *NumChars* é – 1 ou omitido, todos os caracteres ou bytes começando a partir da posição atual são copiados.</span><span class="sxs-lookup"><span data-stu-id="f0a68-121">If the value of *NumChars* is –1, or omitted, all characters or bytes starting from the current position are copied.</span></span>

<span data-ttu-id="f0a68-p104">Se houver caracteres ou bytes existentes no fluxo de destino, todo o conteúdo além do ponto em que a cópia termina permanecerá e não será truncado. **Position** se torna o byte que segue imediatamente o último byte copiado. Se você deseja truncar esses bytes, chame [SetEOS](seteos-method-ado.md).</span><span class="sxs-lookup"><span data-stu-id="f0a68-p104">If there are existing characters or bytes in the destination stream, all contents beyond the point where the copy ends remain, and are not truncated. **Position** becomes the byte immediately following the last byte copied. If you want to truncate these bytes, call [SetEOS](seteos-method-ado.md).</span></span>

<span data-ttu-id="f0a68-p105">**CopyTo** deve ser utilizado para copiar dados para um **Stream** de destino do mesmo tipo que o **Stream** de origem (as definições de sua propriedade **Type** são ambas **adTypeText** ou ambas **adTypeBinary**). Para objetos **Stream** de texto, é possível alterar a definição da propriedade [Charset](charset-property-ado.md) do **Stream** de destino para converter de um conjunto de caracteres para outro. Além disso, objetos **Stream** de texto podem ser copiados com êxito para objetos **Stream** binários, mas objetos **Stream** binários não podem ser copiados para objetos **Stream** de texto.</span><span class="sxs-lookup"><span data-stu-id="f0a68-p105">**CopyTo** should be used to copy data to a destination **Stream** of the same type as the source **Stream** (their **Type** property settings are both **adTypeText** or both **adTypeBinary**). For text **Stream** objects, you can change the [Charset](charset-property-ado.md) property setting of the destination **Stream** to translate from one character set to another. Also, text **Stream** objects can be successfully copied into binary **Stream** objects, but binary **Stream** objects cannot be copied into text **Stream** objects.</span></span>

