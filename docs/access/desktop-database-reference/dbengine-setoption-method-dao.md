---
title: Método DBEngine (DAO)
TOCTitle: SetOption Method
ms:assetid: ea55c10c-2385-1b7e-0cba-32982c9b6643
ms:mtpsurl: https://msdn.microsoft.com/library/Ff836236(v=office.15)
ms:contentKeyID: 48548461
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- dao360.chm1088781
f1_categories:
- Office.Version=v15
ms.openlocfilehash: 5e3a38cb4b35b8472b2c1af601c88af4cc9db813
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/09/2018
ms.locfileid: "25465474"
---
# <a name="dbenginesetoption-method-dao"></a>Método DBEngine (DAO)


**Aplica-se a**: Access 2013 | Office 2013

Substitui temporariamente os valores para as chaves do mecanismo de banco de dados do Microsoft Access no Registro do Windows (somente espaços de trabalho do Microsoft Access).

## <a name="syntax"></a>Sintaxe

*expressão* . SetOption (***opção***, o ***valor***)

*expressão* Uma expressão que retorna um objeto **DBEngine** .

### <a name="parameters"></a>Parâmetros

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Nome</p></th>
<th><p>Obrigatório/Opcional</p></th>
<th><p>Tipo de dados</p></th>
<th><p>Descrição</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>Opção</p></td>
<td><p>Obrigatório</p></td>
<td><p><strong>Long</strong></p></td>
<td><p>Uma constante como descrita em Comentários.</p></td>
</tr>
<tr class="even">
<td><p>Valor</p></td>
<td><p>Obrigatório</p></td>
<td><p><strong>Variant</strong></p></td>
<td><p>O valor que você deseja definir para option.</p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a>Comentários

Cada constante refere-se a chave do registro correspondente no caminho HKEY\_LOCAL\_máquina\\SOFTWARE\\Microsoft\\Office\\12.0\\mecanismo de conectividade do Access\\mecanismos\\bem (ou seja, **dbSharedAsyncDelay** corresponde à tecla HKEY\_LOCAL\_máquina\\SOFTWARE\\Microsoft\\Office\\12.0\\mecanismo de conectividade do Access\\mecanismos\\ACE \\SharedAsyncDelay, e assim por diante).

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Constant</p></th>
<th><p>Descrição</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><strong>dbPageTimeout</strong></p></td>
<td><p>A chave PageTimeout</p></td>
</tr>
<tr class="even">
<td><p><strong>dbSharedAsyncDelay</strong></p></td>
<td><p>A chave SharedAsyncDelay</p></td>
</tr>
<tr class="odd">
<td><p><strong>dbExclusiveAsyncDelay</strong></p></td>
<td><p>A chave ExclusiveAsyncDelay</p></td>
</tr>
<tr class="even">
<td><p><strong>dbLockRetry</strong></p></td>
<td><p>A chave LockRetry</p></td>
</tr>
<tr class="odd">
<td><p><strong>dbUserCommitSync</strong></p></td>
<td><p>A chave UserCommitSync</p></td>
</tr>
<tr class="even">
<td><p><strong>dbImplicitCommitSync</strong></p></td>
<td><p>A chave ImplicitCommitSync</p></td>
</tr>
<tr class="odd">
<td><p><strong>dbMaxBufferSize</strong></p></td>
<td><p>A chave MaxBufferSize</p></td>
</tr>
<tr class="even">
<td><p><strong>dbMaxLocksPerFile</strong></p></td>
<td><p>A chave MaxLocksPerFile</p></td>
</tr>
<tr class="odd">
<td><p><strong>dbLockDelay</strong></p></td>
<td><p>A chave LockDelay</p></td>
</tr>
<tr class="even">
<td><p><strong>dbRecycleLVs</strong></p></td>
<td><p>A chave RecycleLVs</p></td>
</tr>
<tr class="odd">
<td><p><strong>dbFlushTransactionTimeout</strong></p></td>
<td><p>A chave FlushTransactionTimeout</p></td>
</tr>
</tbody>
</table>


Use o método **SetOption** para substituir os valores do Registro no tempo de execução. Novos valores estabelecidos com o método **SetOption** permanecem vigentes até que sejam alterados novamente por outra chamada **SetOption** ou até que o objeto **DBEngine** seja fechado.
