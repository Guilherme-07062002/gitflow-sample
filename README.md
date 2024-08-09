# Gitflow

Pequeno manual de utilização da extensão 'Gitflow Actions Sidebar'.

## O que é Gitflow?

Para mais detalhes acesse: [O que é Gitflow e para que serve](https://www.alura.com.br/artigos/git-flow-o-que-e-como-quando-utilizar?utm_term=&utm_campaign=%5BSearch%5D+%5BPerformance%5D+-+Dynamic+Search+Ads+-+Artigos+e+Conte%C3%BAdos&utm_source=adwords&utm_medium=ppc&hsa_acc=7964138385&hsa_cam=11384329873&hsa_grp=164240702375&hsa_ad=703829337057&hsa_src=g&hsa_tgt=aud-409949667484:dsa-2276348409543&hsa_kw=&hsa_mt=&hsa_net=adwords&hsa_ver=3&gad_source=1&gclid=CjwKCAjw_Na1BhAlEiwAM-dm7FDbp9RzcgqiKR3wWOiDYMCN64bDpnuBd8kys2CK-s0S49zt1eVUzxoCTcsQAvD_BwE)

Em resumo, Gitflow é uma estratégia de versionamento de branchs amplamente utilizada na indústria de desevolvimento de software para garantir a organização no uso do git, principalmente quando se está trabalhando em equipe com várias pessoas manipulando a mesma base de código.

## Instalação

Instale a extensão 'Gitflow Actions Sidebar':

![Extensão Gitflow Actions Sidebar](/imgs/image-3.png)

## Acessando as funcionalidades da extensão

Clique no menu 'Source Control' no menu lateral esquerdo do VSCode:

![Botão source control](/imgs/image-1.png)

Em seguida, expanda o menu 'Gitflow Actions', com isso você terá acesso as funcionalidades da extensão:

![alt text](/imgs/image-2.png)

## Configurando a extensão para o seu repositório

É importante que a extensão identifique quais são cada uma das branchs que você está trabalhando no seu projeto, para isso, clique no '+' ao lado direito do menu 'Gitflow Actions':

![Configurações iniciais](/imgs/image-4.png)

Com isso, será exibido no canto superior da tela uma caixa de texto aonde a extensão irá perguntar sobre as nomenclaturas utilizadas para cada branch no seu repositório, ou seja, o nome da sua branch de produção, desenvolvimento, funcionalidades, correções, releases e etc.

![Informando o nome das branchs utilizadas](/imgs/image-5.png)

## Criando uma nova funcionalidade

Quando for implementar uma nova feature, acesse a branch develop e clique no botão de iniciar em 'Feature':

![Inicializando nova feature](/imgs/image.png)

Será exibido no canto superior da tela uma caixa de texto aonde você poderá informar o nome da feature que será implementada, por exemplo se você irá adicionar algo como um cadastro de usuários, então pode informar na caixa de texto um nome como 'subscribe-users' com isso será criada uma nova branch apartir de develop chamada 'feature/subscribe-users'.

Agora você poderá trabalhar normalmente na branch, subindo os commits e quando finalizar a implementação, será necessário apenas clicar em finalzar feature:

![Finalizar feature](/imgs/image-6.png)

## Lançando uma hotfix

Acesse a branch master e em seguida inicialize uma hotfix de forma semelhante a inicialização de uma feature, conforme é citado no tópico acima. Dê um nome para ela, suba os commits na branch normalmente e por fim, finalize o hotfix.

Com isso a branch hotfix já será mesclada instântaneamente em master, permitindo que o ajuste suba para produção.

## Subindo features em produção

Como vimos mais acima, criamos as funcionalidades apartir da branch de desenvolvimento seguindo o padrão gitflow, diferente dos hotfix que podem ser 'lançados' diretamente em master devido ao fato de geralmente se tratar de pequenos ajustes que provavelmente não irão comprometer ou introduzir nenhum bug ao sistema.

No entanto, após finalizada a implementação de uma feature que foi mesclada em dev, como fazer para subir essa nova atualização em produção?

Para isso, por meio da branch develop, clique em inicializar Release, (de maneira semelhante a como foi feito em feature e hotfix, clicando no botão de play).

![Inicializando release](/imgs/image-7.png)

Após isso, faça alguns testes inicializando a aplicação para garantir que tudo está funcionando de forma adequada, e por fim, após validar que está tudo ok, clique em finalizar release, com isso a modificação será mesclada na master e estará disponivel em produção.