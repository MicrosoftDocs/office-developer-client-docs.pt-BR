---
title: Seção userlist do arquivo de personalização
TOCTitle: Customization File UserList Section
ms:assetid: b60ba3b0-37d4-bb59-d3cd-2ab44d178b8a
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249873(v=office.15)
ms:contentKeyID: 48547263
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: a14060858ad5cd90b410319a515eb271b2b397ea
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/09/2018
ms.locfileid: "25464105"
---
# <a name="customization-file-userlist-section"></a>Seção userlist do arquivo de personalização


**Aplica-se a**: Access 2013 | Office 2013

A seção **userlist** refere-se à seção **se conectar** com o mesmo parâmetro *identifier* de seção.

Esta seção pode conter uma *entrada de acesso de usuário*, que especifica os direitos de acesso do usuário especificado e substitui a *entrada de acesso* do *padrão* na seção **Conectar** correspondentes.

## <a name="syntax"></a>Sintaxe

Uma entrada de acesso de usuário tem este formato:

*userName * * * =* accessRights * * *

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Parte</p></th>
<th><p>Descrição</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><em>userName</em></p></td>
<td><p>O <em>nome de usuário</em> da pessoa que utiliza a conexão. Os nomes válidos de usuário são estabelecidos através da caixa de diálogo <strong>Gerenciador de Serviços</strong> do IIS.</p></td>
</tr>
<tr class="even">
<td><p><strong><em>accessRights</em></strong></p></td>
<td><p>Um dos seguintes direitos de acesso:
<br />
</p>
<ul>
<li><p><strong>NoAccess</strong> — o usuário não pode acessar a fonte de dados.</p></li>
<li><p><strong>ReadOnly</strong> — o usuário pode ler a fonte de dados.</p></li>
<li><p><strong>ReadWrite</strong> — o usuário pode ler a fonte de dados ou gravar nela.</p></li>
</ul>
<p></p></td>
</tr>
</tbody>
</table>

