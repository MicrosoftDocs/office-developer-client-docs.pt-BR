---
title: Método CopyTo (ADO)
TOCTitle: CopyTo method (ADO)
ms:assetid: 1c1ab950-51f7-7ecc-ccd8-e689db02f06a
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248958(v=office.15)
ms:contentKeyID: 48543558
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 2e8de2caf2abc53b0dbd014f21a85a6d54749033
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32295475"
---
# <a name="copyto-method-ado"></a><span data-ttu-id="a34ce-102">Método CopyTo (ADO)</span><span class="sxs-lookup"><span data-stu-id="a34ce-102">CopyTo method (ADO)</span></span>

<span data-ttu-id="a34ce-103">**Aplica-se ao:** Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="a34ce-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="a34ce-104">Copia o número especificado de caracteres ou bytes (dependendo de [Type](type-property-ado-stream.md)) no [Stream](stream-object-ado.md) para outro objeto **Stream**.</span><span class="sxs-lookup"><span data-stu-id="a34ce-104">Copies the specified number of characters or bytes (depending on [Type](type-property-ado-stream.md)) in the [Stream](stream-object-ado.md) to another **Stream** object.</span></span>

## <a name="syntax"></a><span data-ttu-id="a34ce-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="a34ce-105">Syntax</span></span>

<span data-ttu-id="a34ce-106">*Stream*. CopyTo *DestStream*, *NUMCHARS*</span><span class="sxs-lookup"><span data-stu-id="a34ce-106">*Stream*.CopyTo *DestStream*, *NumChars*</span></span>

## <a name="parameters"></a><span data-ttu-id="a34ce-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="a34ce-107">Parameters</span></span>

|<span data-ttu-id="a34ce-108">Parâmetro</span><span class="sxs-lookup"><span data-stu-id="a34ce-108">Parameter</span></span>|<span data-ttu-id="a34ce-109">Descrição</span><span class="sxs-lookup"><span data-stu-id="a34ce-109">Description</span></span>|
|:--------|:----------|
|<span data-ttu-id="a34ce-110">*DestStream*</span><span class="sxs-lookup"><span data-stu-id="a34ce-110">*DestStream*</span></span> |<span data-ttu-id="a34ce-111">Um valor de variável de objeto que contém uma referência para um objeto **Stream** aberto.</span><span class="sxs-lookup"><span data-stu-id="a34ce-111">An object variable value that contains a reference to an open **Stream** object.</span></span> <span data-ttu-id="a34ce-112">O **Stream** atual é copiado para o **Stream** de destino especificado por *DestStream*.</span><span class="sxs-lookup"><span data-stu-id="a34ce-112">The current **Stream** is copied to the destination **Stream** specified by *DestStream*.</span></span> <span data-ttu-id="a34ce-113">O **Stream** de destino já deve estar aberto.</span><span class="sxs-lookup"><span data-stu-id="a34ce-113">The destination **Stream** must already be open.</span></span> <span data-ttu-id="a34ce-114">Se não estiver, ocorrerá um erro em tempo de execução.</span><span class="sxs-lookup"><span data-stu-id="a34ce-114">If not, a run-time error occurs.</span></span><br/><br/><span data-ttu-id="a34ce-115">**Observação**: o parâmetro *DestStream* pode não ser um proxy do objeto **Stream** porque isso requer acesso a uma interface privada no objeto **Stream** que não pode ser remota ao cliente.</span><span class="sxs-lookup"><span data-stu-id="a34ce-115">**NOTE**: The *DestStream* parameter may not be a proxy of the **Stream** object because this requires access to a private interface on the **Stream** object that cannot be remoted to the client.</span></span>|
|<span data-ttu-id="a34ce-116">*NumChars*</span><span class="sxs-lookup"><span data-stu-id="a34ce-116">*NumChars*</span></span> |<span data-ttu-id="a34ce-p102">Opcional. Um valor **Integer** que especifica o número de bytes ou caracteres a serem copiados da posição atual no **Stream** de origem para o **Stream** de destino. O valor padrão é –1, que especifica que todos os caracteres ou bytes são copiados da posição atual até o [EOS](eos-property-ado.md).</span><span class="sxs-lookup"><span data-stu-id="a34ce-p102">Optional. An **Integer** value that specifies the number of bytes or characters to be copied from the current position in the source **Stream** to the destination **Stream**. The default value is –1, which specifies that all characters or bytes are copied from the current position to [EOS](eos-property-ado.md).</span></span>|

## <a name="remarks"></a><span data-ttu-id="a34ce-120">Comentários</span><span class="sxs-lookup"><span data-stu-id="a34ce-120">Remarks</span></span>

<span data-ttu-id="a34ce-p103">Este método copia o número especificado de caracteres ou bytes, iniciando na posição atual especificada pela propriedade [Position](position-property-ado.md). Se o número especificado for maior que o número de bytes disponíveis até o **EOS**, apenas os caracteres ou bytes a partir da posição atual até o **EOS** serão copiados. Se o valor de *NumChars* for –1 ou omitido, todos os caracteres ou bytes a partir da posição atual serão copiados.</span><span class="sxs-lookup"><span data-stu-id="a34ce-p103">This method copies the specified number of characters or bytes, starting from the current position specified by the [Position](position-property-ado.md) property. If the specified number is more than the available number of bytes until **EOS**, then only characters or bytes from the current position to **EOS** are copied. If the value of *NumChars* is –1, or omitted, all characters or bytes starting from the current position are copied.</span></span>

<span data-ttu-id="a34ce-p104">Se houver caracteres ou bytes existentes no fluxo de destino, todo o conteúdo além do ponto em que a cópia termina permanecerá e não será truncado. **Position** se torna o byte que segue imediatamente o último byte copiado. Se você deseja truncar esses bytes, chame [SetEOS](seteos-method-ado.md).</span><span class="sxs-lookup"><span data-stu-id="a34ce-p104">If there are existing characters or bytes in the destination stream, all contents beyond the point where the copy ends remain, and are not truncated. **Position** becomes the byte immediately following the last byte copied. If you want to truncate these bytes, call [SetEOS](seteos-method-ado.md).</span></span>

<span data-ttu-id="a34ce-p105">**CopyTo** deve ser utilizado para copiar dados para um **Stream** de destino do mesmo tipo que o **Stream** de origem (as definições de sua propriedade **Type** são ambas **adTypeText** ou ambas **adTypeBinary**). Para objetos **Stream** de texto, é possível alterar a definição da propriedade [Charset](charset-property-ado.md) do **Stream** de destino para converter de um conjunto de caracteres para outro. Além disso, objetos **Stream** de texto podem ser copiados com êxito para objetos **Stream** binários, mas objetos **Stream** binários não podem ser copiados para objetos **Stream** de texto.</span><span class="sxs-lookup"><span data-stu-id="a34ce-p105">**CopyTo** should be used to copy data to a destination **Stream** of the same type as the source **Stream** (their **Type** property settings are both **adTypeText** or both **adTypeBinary**). For text **Stream** objects, you can change the [Charset](charset-property-ado.md) property setting of the destination **Stream** to translate from one character set to another. Also, text **Stream** objects can be successfully copied into binary **Stream** objects, but binary **Stream** objects cannot be copied into text **Stream** objects.</span></span>

