---
title: Inicializando o driver de fonte de dados do Microsoft Exchange
TOCTitle: Initializing the Microsoft Exchange Data Source driver
ms:assetid: cf87a746-f846-1a01-f4ec-20a25e335193
ms:mtpsurl: https://msdn.microsoft.com/library/Ff834677(v=office.15)
ms:contentKeyID: 48547810
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- acmain11.chm1032667
f1_categories:
- Office.Version=v15
localization_priority: Normal
ms.openlocfilehash: b3460786785ae7b21184b6d96384ecc59e89d287
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32291404"
---
# <a name="initializing-the-microsoft-exchange-data-source-driver"></a>Inicializando o driver de fonte de dados do Microsoft Exchange

**Aplica-se ao:** Access 2013, Office 2013

Quando você instala o driver de fonte de dados do Microsoft Exchange, o programa de instalação grava um conjunto de valores padrão no registro do Microsoft Windows nas subchaves Engines e ISAM formats. Você não deve modificar essas configurações diretamente; use o programa de instalação de seu aplicativo para adicionar, remover ou alterar essas configurações. As seções a seguir descrevem a inicialização e as configurações do ISAM Format no driver de fonte de dados do Microsoft Exchange.

## <a name="microsoft-exchange-data-source-initialization-settings"></a>Configurações de inicialização da fonte de dados do Microsoft Exchange

A pasta **mecanismos\\\\de mecanismo de conectividade do Access do Exchange** inclui configurações de inicialização para o driver Aceexch. dll, usado para acesso externo às pastas do Microsoft Outlook e do Microsoft Exchange. A única entrada dessa pasta é a seguinte:

`win32=<path>\ACEEXCH.DLL`

O mecanismo de banco de dados do Microsoft Access usa esta configuração para indicar a localização do arquivo Aceexch.dll. O caminho completo é determinado no momento da instalação. Os valores são do tipo\_reg sz.

Os resultados de usar o formato ISAM do Outlook e do cliente Exchange são iguais. A única diferença é que os dois clientes diferentes usam nomes diferentes para as mesmas colunas. Os dois formatos ISAM foram criados para que o mecanismo de banco de dados do Microsoft Access possa retornar os nomes de coluna no estilo específico que o usuário deseja.

## <a name="microsoft-outlook-client-isam-formats"></a>Formatos ISAM do cliente Microsoft Outlook

A pasta de **formatos\\\\ISAM do mecanismo de conectividade do Access do Outlook 9,0** contém as entradas a seguir.

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Nome da entrada</p></th>
<th><p>Tipo</p></th>
<th><p>Valor</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>Mecanismo</p></td>
<td><p>REG_SZ</p></td>
<td><p>Exchange</p></td>
</tr>
<tr class="even">
<td><p>ImportFilter</p></td>
<td><p>REG_SZ</p></td>
<td><p>Outlook ()</p></td>
</tr>
<tr class="odd">
<td><p>CanVinculo</p></td>
<td><p>REG_BINARY</p></td>
<td><p>0,01</p></td>
</tr>
<tr class="even">
<td><p>OneTablePerFile</p></td>
<td><p>REG_BINARY</p></td>
<td><p>00</p></td>
</tr>
<tr class="odd">
<td><p>Isamtype</p></td>
<td><p>REG_DWORD</p></td>
<td><p>3D</p></td>
</tr>
<tr class="even">
<td><p>IndexDialog</p></td>
<td><p>REG_BINARY</p></td>
<td><p>00</p></td>
</tr>
<tr class="odd">
<td><p>CreateDBOnExport</p></td>
<td><p>REG_BINARY</p></td>
<td><p>00</p></td>
</tr>
<tr class="even">
<td><p>SupportsLongNames</p></td>
<td><p>REG_BINARY</p></td>
<td><p>0,01</p></td>
</tr>
</tbody>
</table>



> [!NOTE]
> Ao alterar as configurações do Registro do Windows, você deve fechar e reiniciar o mecanismo de banco de dados para que as novas configurações entrem em vigor.



## <a name="microsoft-exchange-client-isam-formats"></a>Formatos ISAM do cliente Microsoft Exchange

A pasta do **Access\\Connectivity Engine\\ISAM formats Exchange 4,0** contém as entradas a seguir.

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Nome da entrada</p></th>
<th><p>Tipo</p></th>
<th><p>Valor</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>Mecanismo</p></td>
<td><p>REG_SZ</p></td>
<td><p>Exchange</p></td>
</tr>
<tr class="even">
<td><p>ImportFilter</p></td>
<td><p>REG_SZ</p></td>
<td><p>Exchange ()</p></td>
</tr>
<tr class="odd">
<td><p>CanVinculo</p></td>
<td><p>REG_BINARY</p></td>
<td><p>0,01</p></td>
</tr>
<tr class="even">
<td><p>OneTablePerFile</p></td>
<td><p>REG_BINARY</p></td>
<td><p>00</p></td>
</tr>
<tr class="odd">
<td><p>Isamtype</p></td>
<td><p>REG_DWORD</p></td>
<td><p>3D</p></td>
</tr>
<tr class="even">
<td><p>IndexDialog</p></td>
<td><p>REG_BINARY</p></td>
<td><p>00</p></td>
</tr>
<tr class="odd">
<td><p>CreateDBOnExport</p></td>
<td><p>REG_BINARY</p></td>
<td><p>00</p></td>
</tr>
<tr class="even">
<td><p>SupportsLongNames</p></td>
<td><p>REG_BINARY</p></td>
<td><p>0,01</p></td>
</tr>
</tbody>
</table>



> [!NOTE]
> Ao alterar as configurações do Registro do Windows, você deve fechar e reiniciar o mecanismo de banco de dados para que as novas configurações entrem em vigor.



## <a name="customizing-the-schemaini-file-for-outlook-and-exchange-data"></a>Personalizando o arquivo Schema. ini para dados do Outlook e do Exchange

O arquivo Schema.ini é usado pelo ISAM do Outlook e do Exchange praticamente da mesma maneira que é usado pelo ISAM de texto. O Schema.ini contém informações específicas da fonte de dados: como os dados são formatados e os nomes das colunas que devem ser acessadas.

Não é necessário modificar o arquivo Schema.ini para ler, importar ou exportar dados do Outlook e do Exchange. Várias das configurações internas do arquivo Schema.ini do Outlook e do Exchange são específicas das tags internas que o MAPI exige. Você não deve tentar modificar os valores dessas tags.

