---
title: Método ConvertToString (RDS)
TOCTitle: ConvertToString Method (RDS)
ms:assetid: dc6381e4-98c8-badc-ad8c-87c70574a8a4
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250113(v=office.15)
ms:contentKeyID: 48548136
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 0820aec3ce8606f5f8f0fcb8dac838ae7bbd15d8
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/31/2018
ms.locfileid: "25869124"
---
# <a name="converttostring-method-rds"></a><span data-ttu-id="b861b-102">Método ConvertToString (RDS)</span><span class="sxs-lookup"><span data-stu-id="b861b-102">ConvertToString Method (RDS)</span></span>


<span data-ttu-id="b861b-103">**Aplica-se a**: Access 2013, o Office 2013</span><span class="sxs-lookup"><span data-stu-id="b861b-103">**Applies to**: Access 2013, Office 2013</span></span> 

<span data-ttu-id="b861b-104">Converte um [Recordset](recordset-object-ado.md) em uma sequência MIME que representa os dados do conjunto de registros.</span><span class="sxs-lookup"><span data-stu-id="b861b-104">Converts a [Recordset](recordset-object-ado.md) to a MIME string that represents the recordset data.</span></span>

## <a name="syntax"></a><span data-ttu-id="b861b-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="b861b-105">Syntax</span></span>

<span data-ttu-id="b861b-106">*DataFactory*. ConvertToString (*Recordset*)</span><span class="sxs-lookup"><span data-stu-id="b861b-106">*DataFactory*.ConvertToString(*Recordset*)</span></span>

## <a name="parameters"></a><span data-ttu-id="b861b-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="b861b-107">Parameters</span></span>

  - <span data-ttu-id="b861b-108">*DataFactory*</span><span class="sxs-lookup"><span data-stu-id="b861b-108">*DataFactory*</span></span>

  - <span data-ttu-id="b861b-109">Uma variável de objeto que representa um objeto [RDSServer.DataFactory](datafactory-object-rdsserver.md).</span><span class="sxs-lookup"><span data-stu-id="b861b-109">An object variable that represents an [RDSServer.DataFactory](datafactory-object-rdsserver.md) object.</span></span>

  - <span data-ttu-id="b861b-110">*Recordset*</span><span class="sxs-lookup"><span data-stu-id="b861b-110">*Recordset*</span></span>

  - <span data-ttu-id="b861b-111">Uma variável de objeto que representa um objeto **Recordset**.</span><span class="sxs-lookup"><span data-stu-id="b861b-111">An object variable that represents a **Recordset** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="b861b-112">Comentários</span><span class="sxs-lookup"><span data-stu-id="b861b-112">Remarks</span></span>

<span data-ttu-id="b861b-113">Com arquivos .asp, utilize **ConvertToString** para inserir o **Recordset** em uma página HTML gerada no servidor para transportá-la para um computador cliente.</span><span class="sxs-lookup"><span data-stu-id="b861b-113">With .asp files, use **ConvertToString** to embed the **Recordset** in an HTML page generated on the server to transport it to a client computer.</span></span>

<span data-ttu-id="b861b-114">**ConvertToString** primeiro carrega o **Recordset** nas tabelas de Serviço de Cursor e, em seguida, gera um fluxo no formato MIME.</span><span class="sxs-lookup"><span data-stu-id="b861b-114">**ConvertToString** first loads the **Recordset** into the Cursor Service tables, and then generates a stream in MIME format.</span></span>

<span data-ttu-id="b861b-p101">No cliente, o Remote Data Service pode converter a sequência MIME de volta em um **Recordset** totalmente funcional. Isso funciona bem para tratar menos de 400 linhas de dados com não mais de 1024 bytes de largura por linha. Você não deve utilizá-lo para efetuar o streaming de dados BLOB e grandes conjuntos de resultado por HTTP. Nenhuma compactação em fio é executada na sequência, portanto conjuntos de dados muito grandes levarão um tempo considerável para transporte por HTTP quando comparados ao formato de tabela otimizada para fio definido e implementado pelo Remote Data Service como seu formato de protocolo de transporte nativo.</span><span class="sxs-lookup"><span data-stu-id="b861b-p101">On the client, Remote Data Service can convert the MIME string back into a fully functioning **Recordset**. It works well for handling fewer than 400 rows of data with no more than 1024 bytes width per row. You shouldn't use it for streaming BLOB data and large result sets over HTTP. No wire compression is performed on the string, so very large data sets will take considerable time to transport over HTTP when compared to the wire-optimized tablegram format defined and deployed by Remote Data Service as its native transport protocol format.</span></span>


> [!NOTE]
> <span data-ttu-id="b861b-p102">[!OBSERVAçãO] Se estiver utilizando Active Server Pages para inserir a sequência MIME resultante em uma página HTML cliente, esteja ciente de que as versões do VBScript anteriores à versão 2.0 limitam o tamanho da sequência a 32K. Se esse limite for excedido, será retornado um erro. Mantenha o escopo da consulta relativamente pequeno ao utilizar inserção de MIME utilizando arquivos .asp. Para corrigir isso, baixe a versão mais recente do VBScript na [Centro de Download da Microsoft](https://www.microsoft.com/downloads/en/default.aspx).</span><span class="sxs-lookup"><span data-stu-id="b861b-p102">If you are using Active Server Pages to embed the resulting MIME string in a client HTML page, be aware that versions of VBScript earlier than version 2.0 limit the string's size to 32K. If this limit is exceeded, an error is returned. Keep the query scope relatively small when using MIME embedding via .asp files. To fix this, download the latest version of VBScript from the [Microsoft Download Center](https://www.microsoft.com/downloads/en/default.aspx).</span></span>


