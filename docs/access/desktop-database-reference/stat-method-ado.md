---
title: Método Stat - ActiveX Data Objects (ADO)
TOCTitle: Stat method (ADO)
ms:assetid: d3d3976b-14d4-dee0-412d-a37bc72fbfd3
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250056(v=office.15)
ms:contentKeyID: 48547916
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 853d89bde9184bd546b3e7df9e8eda287faf86c9
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32308544"
---
# <a name="stat-method-ado"></a>Método Stat (ADO)

**Aplica-se ao:** Access 2013, Office 2013

Recupera informações sobre um objeto **Stream**.

## <a name="syntax"></a>Sintaxe

Fluxo *longo.* Stat(*StatStg*, *StatFlag*)

## <a name="return-value"></a>Valor de retorno

Um valor long que indica o status da operação.

## <a name="parameters"></a>Parâmetros

|Parâmetro|Descrição|
|:--------|:----------|
|*StatStg* |Uma estrutura STATSTG que será preenchida com informações sobre o fluxo. A implementação do método Stat utilizada pelo objeto Stream do ADO não preenche todos os campos da estrutura.|
|*StatFlag* |Especifica que este método não retorna alguns dos membros na estrutura STATSTG, economizando dessa forma uma operação de alocação de memória. Os valores são obtidos da enumeração STATFLAG.<br/><br/>A enumeração STATFLAG tem dois valores:<br/>- STATFLAG_DEFAULT: 0<br/>- STATFLAG_NONAME: 1 |


## <a name="remarks"></a>Comentários

A versão do método Stat implementada para o objeto Stream do ADO preenche os seguintes campos da estrutura STATSTG:

|Campo|Descrição|
|:--------|:----------|
|*pwcsName* |Uma cadeia de caracteres que contém o nome do fluxo, se um estiver disponível e o valor StatFlag NONAME não \_ foi especificado.|
|*cbSize* |Especifica o tamanho em bytes do fluxo ou matriz de bytes.|
|*mtime* |Indica a hora da última modificação para esse repositório, fluxo ou matriz de bytes.|
|*ctime* |Indica a hora da criação para esse repositório, fluxo ou matriz de bytes.|
|*atime* |Indica a hora do último acesso para esse repositório, fluxo ou matriz de bytes.|

Se STATFLAG NONAME for especificado no parâmetro \_ StatFlag, o nome do fluxo não será retornado.

Se STATFLAG NONAME não foi especificado no parâmetro StatFlag e não há nenhum nome disponível para o fluxo atual, esse valor será \_ E \_ NOTIMPL.

