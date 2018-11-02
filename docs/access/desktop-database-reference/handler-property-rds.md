---
title: Propriedade Handler (RDS)
TOCTitle: Handler property (RDS)
ms:assetid: aaf8c8c6-f95b-3cf3-b3f6-203f37464c87
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249792(v=office.15)
ms:contentKeyID: 48546962
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 2bb9444091611fbd051da9fa649b5d3efdb92ee6
ms.sourcegitcommit: d7248f803002b31cf7fc561b03530199a9b0a8fd
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/02/2018
ms.locfileid: "25923578"
---
# <a name="handler-property-rds"></a><span data-ttu-id="b967c-102">Propriedade Handler (RDS)</span><span class="sxs-lookup"><span data-stu-id="b967c-102">Handler property (RDS)</span></span>


<span data-ttu-id="b967c-103">**Aplica-se a**: Access 2013, o Office 2013</span><span class="sxs-lookup"><span data-stu-id="b967c-103">**Applies to**: Access 2013, Office 2013</span></span>


<span data-ttu-id="b967c-104">Indica o nome de um programa de personalização do servidor (manipulador) que estende a funcionalidade do [RDSServer.DataFactory](datafactory-object-rdsserver.md) e qualquer parâmetro usado pelo *manipulador*.</span><span class="sxs-lookup"><span data-stu-id="b967c-104">Indicates the name of a server-side customization program (handler) that extends the functionality of the [RDSServer.DataFactory](datafactory-object-rdsserver.md), and any parameters used by the *handler*.</span></span>

## <a name="syntax"></a><span data-ttu-id="b967c-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="b967c-105">Syntax</span></span>

<span data-ttu-id="b967c-106">*DataControl*. Manipulador = *cadeia de caracteres*</span><span class="sxs-lookup"><span data-stu-id="b967c-106">*DataControl*.Handler = *String*</span></span>

## <a name="parameters"></a><span data-ttu-id="b967c-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="b967c-107">Parameters</span></span>

  - <span data-ttu-id="b967c-108">*DataControl*</span><span class="sxs-lookup"><span data-stu-id="b967c-108">*DataControl*</span></span>

  - <span data-ttu-id="b967c-109">Uma variável de objeto que representa um objeto [RDS.DataControl](datacontrol-object-rds.md).</span><span class="sxs-lookup"><span data-stu-id="b967c-109">An object variable that represents an [RDS.DataControl](datacontrol-object-rds.md) object.</span></span>

  - <span data-ttu-id="b967c-110">*String*</span><span class="sxs-lookup"><span data-stu-id="b967c-110">*String*</span></span>

  - <span data-ttu-id="b967c-111">Um valor **String** que contém o nome do manipulador e qualquer parâmetro, todos separado por vírgulas (por exemplo, "handlerName, parm1, parm2,..., parm *N"*).</span><span class="sxs-lookup"><span data-stu-id="b967c-111">A **String** value that contains the name of the handler and any parameters, all separated by commas (for example, "handlerName,parm1,parm2,...,parm *N*" ).</span></span>

## <a name="remarks"></a><span data-ttu-id="b967c-112">Comentários</span><span class="sxs-lookup"><span data-stu-id="b967c-112">Remarks</span></span>

<span data-ttu-id="b967c-113">Esta propriedade oferece suporte à personalização, uma funcionalidade que requer a definição da propriedade [CursorLocation](cursorlocation-property-ado.md) como **adUseClient**.</span><span class="sxs-lookup"><span data-stu-id="b967c-113">This property supports customization, a functionality that requires setting the [CursorLocation](cursorlocation-property-ado.md) property to **adUseClient**.</span></span>

<span data-ttu-id="b967c-p101">O nome do manipulador e seus parâmetros, se houver, são separados por vírgulas (","). Um comportamento imprevisível ocorrerá se um ponto-e-vírgula (";") aparecer em qualquer lugar dentro do *String*. Você pode compor seu próprio manipulador, desde que ele ofereça suporte à interface **IDataFactoryHandler**.</span><span class="sxs-lookup"><span data-stu-id="b967c-p101">The name of the handler and its parameters, if any, are separated by commas (","). Unpredictable behavior will result if a semicolon (";") appears anywhere within *String*. You can write your own handler, provided it supports the **IDataFactoryHandler** interface.</span></span>

<span data-ttu-id="b967c-p102">O nome do manipulador padrão é **MSDFMAP.Handler** e seu parâmetro padrão é um arquivo de personalização chamado **MSDFMAP.INI**. Use esta propriedade para invocar arquivos de personalização alternativos pelo administrador do servidor.</span><span class="sxs-lookup"><span data-stu-id="b967c-p102">The name of the default handler is **MSDFMAP.Handler**, and its default parameter is a customization file named **MSDFMAP.INI**. Use this property to invoke alternate customization files created by your server administrator.</span></span>

<span data-ttu-id="b967c-119">A alternativa para definir a propriedade **Handler** é especificar um manipulador e os parâmetros na propriedade [ConnectionString](connectionstring-property-ado.md) ; ou seja, "\**manipulador = \* \* \* handlerName, parm1, parm2,...;*".</span><span class="sxs-lookup"><span data-stu-id="b967c-119">The alternative to setting the **Handler** property is to specify a handler and parameters in the [ConnectionString](connectionstring-property-ado.md) property; that is, "\**Handler=\*\*\*handlerName,parm1,parm2,...;*".</span></span>

