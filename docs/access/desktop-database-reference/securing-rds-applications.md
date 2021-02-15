---
title: Protegendo aplicativos RDS
TOCTitle: Securing RDS Applications
ms:assetid: 15f41cbb-d6e0-aca8-9c3a-97516d82c302
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248922(v=office.15)
ms:contentKeyID: 48543423
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 4a531c01750117ae7abbf87e5ba4cb23daf37851
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32308774"
---
# <a name="securing-rds-applications"></a>Protegendo aplicativos RDS

**Aplica-se ao:** Access 2013, Office 2013

## <a name="microsoft-internet-explorer-security-issues"></a>Problemas de segurança do Microsoft Internet Explorer

Com novas melhorias de segurança adicionadas ao Microsoft Internet Explorer, alguns objetos ADO e RDS estão restritos à execução apenas em um ambiente de modo "seguro". Isso requer atenção aos problemas que incluem zonas diferentes, níveis de segurança, comportamento restritivo, operações não seguras e configurações de segurança personalizadas.

Para obter mais informações sobre esses problemas, consulte ADO and RDS Security Issues in Microsoft Internet Explorer (Problemas de segurança de ADO e RDS no Microsoft Internet Explorer) nos Artigos técnicos sobre o ADO (ActiveX Data Objects).

## <a name="security-and-your-web-server"></a>Segurança e seu servidor Web

Se você usar o [objeto RDSServer.DataFactory](datafactory-object-rdsserver.md) em seu servidor Web da Internet, lembre-se de que isso cria um potencial risco à segurança. Os usuários externos que obtêm DSN (Data Source Name, Nome da Fonte de Dados), Identificação do usuário e informações de senha válidos podem criar páginas para enviar quaisquer consultas a essa fonte de dados. Se você quiser acesso mais restrito à fonte de dados, uma opção é cancelar o registro e excluir o objeto **RDSServer.DataFactory** (msadcf.dll) e, no lugar, usar objetos comerciais personalizados com consultas embutidas em código.

Para obter mais informações sobre as implicações de segurança do uso do objeto RDSServer.DataFactory, consulte o Boletim de Segurança da Microsoft MS99-025 no site de Segurança da [Microsoft.](https://www.microsoft.com/en-us/security/default.aspx)

## <a name="client-impersonation-and-security"></a>Representação de cliente e segurança

Se  a propriedade Autenticação de Senha do seu servidor Web do IIS estiver definida como autenticação de Desafio/Resposta do Windows NT (para Windows NT 4.0) ou como autenticação integrada do Windows (para Windows 2000), os objetos de negócios serão invocados no contexto de segurança do cliente. Esse é um novo recurso no RDS 1.5 que permite a Representação de cliente em HTTP. Ao trabalhar nesse modo, o logon no servidor Web (IIS) não é anônimo, mas usa a ID de usuário e a senha em que o computador cliente está sendo executado. Se os DSNs ODBC estiverem configurados para usar Conexão confiável, o acesso aos bancos de dados, como SQL Server, também ocorrerá de acordo com o contexto de segurança do cliente. Mas isso funcionará somente se o banco de dados estiver no mesmo computador que o IIS; as credenciais do cliente não podem ser transportadas para nenhum outro computador.

Por exemplo, um cliente, John Doe, com ID de usuário="JohnD" e senha="secret" está conectado a um computador cliente. Ele executa um aplicativo, com base em navegador, que precisa acessar o objeto **RDSServer.DataFactory** para criar um [Recordset](recordset-object-ado.md) por meio da execução de uma consulta SQL no computador "MyServer" que executa o IIS. MyServer, um sistema que executa o Windows NT Server 4.0, é configurado para usar a Autenticação de desafio/resposta do Windows NT, a opção "Usar conexão confiável" do DSN ODBC está selecionada e o servidor também contém a fonte de dados SQL Server. Quando uma solicitação é recebida no servidor Web, ela solicita ao cliente a ID de usuário e a senha. Portanto, a solicitação é registrada em MeuServidor como proveniente de "JohnD"/"Secret" em vez de IUSER MyServer (que é o padrão quando a Autenticação de Senha Anônima está \_ on). De modo semelhante, "JohnD"/"Secret" é utilizado quando é feita a conexão no SQL Server.

Consequentemente, o modo Autenticação de desafio/resposta do Windows NT para IIS permite a criação de páginas HTML sem que o usuário seja explicitamente solicitado a informar a identificação do usuário e a senha necessárias para o logon no banco de dados. Se a Autenticação básica do IIS estiver sendo utilizada, isso também será exigido.

## <a name="password-authentication"></a>Autenticação de senha

O RDS pode se comunicar com um servidor Web do IIS em execução em qualquer um dos três modos de Autenticação de Senha: Autenticação anônima, básica ou de desafio/resposta do NT (chamada de autenticação integrada do Windows no Windows 2000). Essas configurações definem como um servidor Web controla o acesso através dele, como exigir que um computador cliente tenha privilégios de acesso explícitos no servidor Web NT.

