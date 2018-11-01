---
title: Propriedade Connection.Connect (DAO)
TOCTitle: Connect Property
ms:assetid: 58b514a2-91cd-7918-cba5-15d71c2457a6
ms:mtpsurl: https://msdn.microsoft.com/library/Ff194335(v=office.15)
ms:contentKeyID: 48545001
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 8dc64341ddd48f9f973354c162811dd7f8eb6f3f
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/31/2018
ms.locfileid: "25886890"
---
# <a name="connectionconnect-property-dao"></a>Propriedade Connection.Connect (DAO)


**Aplica-se a**: Access 2013, o Office 2013

Define ou retorna um valor que fornece informações sobre a origem de uma conexão aberta. **String** de leitura/gravação.

## <a name="syntax"></a>Sintaxe

*expressão* . Conecte-se

*expressão* Uma variável que representa um objeto de **Conexão** .

## <a name="remarks"></a>Comentários

A configuração da propriedade **Connect** é uma **String** composta por um especificador de tipo de banco de dados e nenhum ou mais parâmetros separados por ponto-e-vírgula. A propriedade **Connect** transmite informações adicionais para o ODBC e certos drivers do ISAM, conforme necessário.

Para executar uma consulta passagem SQL em uma tabela vinculada ao arquivo de banco de dados do Microsoft Access, você deve primeiro definir a propriedade **Connect** do banco de dados da tabela vinculada para uma sequência de conexão ODBC válida.

Para um objeto **TableDef** que representa uma tabela vinculada, a configuração da propriedade **Connect** consiste em uma ou duas partes (um especificador de tipo de banco de dados e um caminho para o banco de dados), que terminam com um ponto-e-vírgula.

O caminho, como mostrado na tabela a seguir, é um caminho completo para o diretório que contém os arquivos de banco de dados e deve ser precedido pelo identificador DATABASE=. Em alguns casos (como os bancos de dados do mecanismo de banco de dados do Microsoft Excel e do Microsoft Access), você deve incluir um nome de arquivo específico no argumento do caminho do banco de dados.

A tabela a seguir mostra os tipos possíveis de bancos de dados e seus especificadores e caminhos correspondentes para a configuração da propriedade **Connect**. Em um espaço de trabalho ODBCDirect, somente o especificador "ODBC" pode ser utilizado.

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Tipo de banco de dados</p></th>
<th><p>Especificador</p></th>
<th><p>Exemplo</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>Banco de dados do Microsoft Access</p></td>
<td><p>[database;]</p></td>
<td><p>drive:\path\filename</p></td>
</tr>
<tr class="even">
<td><p>dBASE III</p></td>
<td><p>dBASE III;</p></td>
<td><p>unidade: \path</p></td>
</tr>
<tr class="odd">
<td><p>dBASE IV</p></td>
<td><p>dBASE IV;</p></td>
<td><p>unidade: \path</p></td>
</tr>
<tr class="even">
<td><p>dBASE 5</p></td>
<td><p>dBASE 5.0;</p></td>
<td><p>unidade: \path</p></td>
</tr>
<tr class="odd">
<td><p>Paradox 3.x</p></td>
<td><p>Paradox 3.x;</p></td>
<td><p>unidade: \path</p></td>
</tr>
<tr class="even">
<td><p>Paradox 4.x</p></td>
<td><p>Paradox 4.x;</p></td>
<td><p>unidade: \path</p></td>
</tr>
<tr class="odd">
<td><p>Paradox 5.x</p></td>
<td><p>Paradox 5.x;</p></td>
<td><p>unidade: \path</p></td>
</tr>
<tr class="even">
<td><p>Microsoft Excel 3.0</p></td>
<td><p>Excel 3.0;</p></td>
<td><p>drive:\path\filename.xls</p></td>
</tr>
<tr class="odd">
<td><p>Microsoft Excel 4.0</p></td>
<td><p>Excel 4.0;</p></td>
<td><p>drive:\path\filename.xls</p></td>
</tr>
<tr class="even">
<td><p>Microsoft Excel 5.0 ou Microsoft Excel 95</p></td>
<td><p>Excel 5.0;</p></td>
<td><p>drive:\path\filename.xls</p></td>
</tr>
<tr class="odd">
<td><p>Microsoft Excel 97</p></td>
<td><p>Excel 8.0;</p></td>
<td><p>drive:\path\filename.xls</p></td>
</tr>
<tr class="even">
<td><p>Lotus 1-2-3 WKS e WK1</p></td>
<td><p>Lotus WK1;</p></td>
<td><p>drive:\path\filename.wk1</p></td>
</tr>
<tr class="odd">
<td><p>Lotus 1-2-3 WK3</p></td>
<td><p>Lotus WK3;</p></td>
<td><p>drive:\path\filename.wk3</p></td>
</tr>
<tr class="even">
<td><p>Lotus 1-2-3 WK4</p></td>
<td><p>Lotus WK4;</p></td>
<td><p>drive:\path\filename.WK4</p></td>
</tr>
<tr class="odd">
<td><p>HTML Import</p></td>
<td><p>HTML Import;</p></td>
<td><p>drive:\path\filename</p></td>
</tr>
<tr class="even">
<td><p>HTML Export</p></td>
<td><p>HTML Export;</p></td>
<td><p>unidade: \path</p></td>
</tr>
<tr class="odd">
<td><p>Texto</p></td>
<td><p>Texto;</p></td>
<td><p>unidade: \path</p></td>
</tr>
<tr class="even">
<td><p>ODBC</p></td>
<td><p>ODBC; Banco de dados = database; UID = user; PWD = password; DSN = datasourcename; [LOGINTIMEOUT = seconds;]</p></td>
<td><p>Nenhum</p></td>
</tr>
<tr class="odd">
<td><p>Microsoft Exchange</p></td>
<td><p>Exchange 4.0; MAPILEVEL = folderpath; [TABLETYPE = {0 | 1}]; [Perfil = profile;] [PWD = password;] [Banco de dados = database;]</p></td>
<td><p>drive:\path\filename</p></td>
</tr>
</tbody>
</table>


Se o especificador for apenas "ODBC;", o driver ODBC exibirá uma caixa de diálogo listando todos os nomes registrados de fonte de dados ODBC para que o usuário possa selecionar um banco de dados.

Se uma senha for solicitada, mas não for fornecida na configuração da propriedade **Connect**, uma caixa de diálogo de login será exibida na primeira vez em que a tabela for acessada pelo driver ODBC e novamente se a conexão for fechada e reaberta.

Para dados no Microsoft Exchange, a chave MAPILEVEL exigida deve estar definida como um caminho de pasta totalmente resolvido (por exemplo, "Mailbox - Pat SmithIAlpha/Today"). O caminho não inclui o nome da pasta que será aberta como uma tabela; em vez disso, o nome dessa pasta deve ser especificado como o argumento nome para o método **CreateTable** . A chave TABLETYPE deve estar definida como "0" para abrir a pasta (padrão) ou "1" para abrir um catálogo de endereços. A chave PROFILE é padronizada para o perfil atualmente em uso.

Para as tabelas base em um banco de dados do Microsoft Access, a definição da propriedade **Connect** será uma sequência de caracteres com comprimento zero ("").

Você pode definir a propriedade **Connect** para um objeto de **banco de dados** , fornecendo um argumento de origem para o método **OpenDatabase** . Você pode verificar a configuração para determinar o tipo, o caminho, a identificação do usuário, a senha ou a fonte de dados ODBC do banco de dados.

Em um objeto **QueryDef** no espaço de trabalho do Microsoft Access, você pode usar a propriedade **Connect** com a propriedade ReturnsRecords para criar uma consulta passagem ODBC SQL. Databasetype da cadeia de caracteres de conexão for "ODBC;", e o restante da cadeia de caracteres contém informações específicas para o driver ODBC usado para acessar os dados remotos. Para obter mais informações, consulte a documentação do driver específico.


> [!NOTE]
> - Você deve definir a propriedade **Connect** antes de definir a propriedade **ReturnsRecords**.
> - Você deve ter permissão de acesso ao computador que contém o servidor de banco de dados que está tentando acessar.


