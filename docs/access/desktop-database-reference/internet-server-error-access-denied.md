---
title: 'Erro do servidor de Internet: Acesso negado'
TOCTitle: 'Internet Server Error: Access Denied'
ms:assetid: 65f4608b-afec-2867-dae3-e29bae03a6fd
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249395(v=office.15)
ms:contentKeyID: 48545334
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: c874b7a2c4facb9f5969bf9a2150c86773a2687a
ms.sourcegitcommit: a49b77f4c8cec69f90656a86f0872cf34c35968e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/17/2018
ms.locfileid: "25603340"
---
# <a name="internet-server-error-access-denied"></a>Erro do servidor de Internet: Acesso negado


**Aplica-se a**: Access 2013 | Office 2013

Se você receber este erro, geralmente significa que o Microsoft Internet Information Services (IIS) retornou o seguinte status:

HTTP\_STATUS\_NEGADOS 401

<<<<<<< Cabeça Verifique se os diretórios acessados pelo IIS têm permissões adequadas. O RDS pode se comunicar com um servidor Web IIS em qualquer um dos modos de Autenticação de senha: Anônimo, Básico ou Resposta/Desafio NT (chamado de autenticação integrada do Windows no Windows 2000). Além disso, o servidor Web deve ter permissões para o computador da origem de dados se for um computador com Windows NT/Windows 2000.
=== Verifique se os diretórios acessados pelo IIS possui permissões adequadas. RDS podem se comunicar com um servidor de web IIS executando em qualquer um dos três modos de autenticação de senha: anônima, básica ou o desafio/resposta do NT (chamado de autenticação integrada do Windows no Windows 2000). Além disso, o servidor web deve ter permissões para o computador de origem de dados, caso se trate de um computador Windows NT/Windows 2000.
>>>>>>> mestre

