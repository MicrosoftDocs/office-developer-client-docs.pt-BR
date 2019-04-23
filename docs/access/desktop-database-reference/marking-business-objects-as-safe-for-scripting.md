---
title: Marcação de objetos Business como confiáveis para script
TOCTitle: Marking business objects as safe for scripting
ms:assetid: 8ee49aec-672d-96f7-baa6-9261317a4d90
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249630(v=office.15)
ms:contentKeyID: 48546295
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: fe5d331b7f3ab4685cb930323076d111a25ec68e
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32289774"
---
# <a name="marking-business-objects-as-safe-for-scripting"></a>Marcação de objetos Business como confiáveis para script

**Aplica-se ao:** Access 2013, Office 2013

Para ajudar a assegurar um ambiente seguro de Internet, você precisa marcar todos os objetos de negócios instanciados com o método [CreateObject](dataspace-object-rds.md) do objeto [RDS.DataSpace](createobject-method-rds.md) como "seguro para script". Você precisa se assegurar de que estejam marcados dessa forma na área de Licença no Registro do sistema antes que possam ser utilizados no DCOM.

Para marcar manualmente seu objeto de negócios como seguro para script, crie um arquivo de texto com uma extensão .reg que contenha o seguinte texto. Os dois números a seguir permitem o recurso seguro-para-script:

```vb 
 
[HKEY_CLASSES_ROOT\CLSID\<MyActiveXGUID>\Implemented 
Categories\{7DD95801-9882-11CF-9FA9-00AA006C42C4}] 
[HKEY_CLASSES_ROOT\CLSID\<MyActiveXGUID>\Implemented 
Categories\{7DD95802-9882-11CF-9FA9-00AA006C42C4}] 
```

onde \< *MyActiveXGUID* \> é o número GUID hexadecimal do seu objeto de negócios. Salve-o e misture-o em seu registro, usando o Editor de Registro ou dando um clique duplo no arquivo .reg no Windows Explorer.

Os objetos de negócios criados no Microsoft Visual Basic podem ser automaticamente marcados como "seguros para scripts" com o assistente de implantação e pacote. Quando o assistente solicitar que especifique as definições de segurança, selecione **Seguro para Inicialização** e **Seguro para Script**.

Na última etapa, o assistente de configuração do aplicativo cria um arquivo .htm e um arquivo .cab. Em seguida, você pode copiar esses dois arquivos para o computador de destino e dar um clique duplo no arquivo .htm para carregar a página e registrar corretamente o servidor.

Como o objeto de negócios será instalado no diretório Windows\\system32\\Occache por padrão, mova-o para o diretório\\system32 do Windows e altere **o\_CLSID\_\\\\ raiz classe de hKey** \<Chave do registro *MyActiveXGUID*\>\\**InprocServer32** para corresponder ao caminho correto.


> [!NOTE]
> [!OBSERVAçãO] Os objetos de negócios marcados como seguros para script ou seguros para inicialização podem ser instanciados e inicializados por qualquer pessoa na rede. Qualquer objeto de negócios personalizado não deve ser projetado e implementado casualmente. É obrigatório que tais objetos não representem uma ameaça de segurança que os hackers possam explorar para ganhar acesso à área sensível do servidor hospedeiro e infligir danos.


