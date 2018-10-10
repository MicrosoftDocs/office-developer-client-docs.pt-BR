---
title: Marcando os objetos de negócios como seguros para o script
TOCTitle: Marking Business Objects as Safe for Scripting
ms:assetid: 8ee49aec-672d-96f7-baa6-9261317a4d90
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249630(v=office.15)
ms:contentKeyID: 48546295
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 7ac928f7e61cf633aac6963565cf3aae441a2ac6
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/09/2018
ms.locfileid: "25464770"
---
# <a name="marking-business-objects-as-safe-for-scripting"></a>Marcando os objetos de negócios como seguros para o script


**Aplica-se a**: Access 2013 | Office 2013

Para ajudar a assegurar um ambiente seguro de Internet, você precisa marcar todos os objetos de negócios instanciados com o método [CreateObject](dataspace-object-rds.md) do objeto [RDS.DataSpace](createobject-method-rds.md) como "seguro para script". Você precisa se assegurar de que estejam marcados dessa forma na área de Licença no Registro do sistema antes que possam ser utilizados no DCOM.

Para marcar manualmente seu objeto de negócios como seguro para script, crie um arquivo de texto com uma extensão .reg que contenha o seguinte texto. Os dois números a seguir permitem o recurso seguro-para-script:

```vb 
 
[HKEY_CLASSES_ROOT\CLSID\<MyActiveXGUID>\Implemented 
Categories\{7DD95801-9882-11CF-9FA9-00AA006C42C4}] 
[HKEY_CLASSES_ROOT\CLSID\<MyActiveXGUID>\Implemented 
Categories\{7DD95802-9882-11CF-9FA9-00AA006C42C4}] 
```

onde \< *MyActiveXGUID* \> é o número hexadecimal de GUID de seu objeto de negócios. Salve-o e misture-o em seu registro, usando o Editor de Registro ou dando um clique duplo no arquivo .reg no Windows Explorer.

Os objetos de negócios criados no Microsoft® Visual Basic podem ser automaticamente marcados como "seguros para script" com o assistente de pacote e de implementação. Quando o assistente solicitar que especifique as definições de segurança, selecione **Seguro para Inicialização** e **Seguro para Script**.

Na última etapa, o assistente de configuração do aplicativo cria um arquivo .htm e um arquivo .cab. Em seguida, você pode copiar esses dois arquivos para o computador de destino e dar um clique duplo no arquivo .htm para carregar a página e registrar corretamente o servidor.

Porque o objeto comercial será instalado no Windows\\System32\\Occache diretório por padrão, movê-lo para o Windows\\diretório System32 e altere o **HKEY\_CLASSES\_raiz\\CLSID\\ ** \< *MyActiveXGUID*\>\\chave do registro**InprocServer32** para coincidir com o caminho correto.


> [!NOTE]
> [!OBSERVAçãO] Os objetos de negócios marcados como seguros para script ou seguros para inicialização podem ser instanciados e inicializados por qualquer pessoa na rede. Qualquer objeto de negócios personalizado não deve ser projetado e implementado casualmente. É obrigatório que tais objetos não representem uma ameaça de segurança que os hackers possam explorar para ganhar acesso à área sensível do servidor hospedeiro e infligir danos.

