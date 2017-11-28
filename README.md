# План выступления

## О Cardano

1. Что это такое, кто и когда это создал, когда это релизнулось?
2. Зачем нам ещё одна криптовалюта?

## Почему Haskell: выбор правильного инструмента

1. Криптовалютная система - то, где сияют все сильные стороны Haskell.

* Сильная статическая типизация и чистота -> корректность кода
* Выразительные типы и полиморфизм        -> гибкость кода
* нативная компилируемость                -> высокая эффективность выполнения кода ноды сети + простой установочник
* параллельный и конкурентный код         -> ещё более высокая эффективность выполнения кода
* много хороших библиотек
* предсказуемая и воспроизводимая сборка  -> (Nix + Haskell = дружба навек)

## Заглянем под капот: show me the code

1. Показать красивые типы из core/pos/Core/Types.hs... Sum-типы и прочее.
2. Что-нибудь про кондуиты, возможно.
3. NonEmpty входов/выходов у транзакции.
4. Фантомные типы для гибкости алгоритмов.





















Cardano is a project that began in 2015 as an effort to change the way cryptocurrencies are designed and developed. The overall focus beyond a particular set of innovations is to provide a more balanced and sustainable ecosystem that better accounts for the needs of its users as well as other systems seeking integration.

In the spirit of many open source projects, Cardano did not begin with a comprehensive roadmap or even an authoritative white paper. Rather it embraced a collection of design principles, engineering best practices and avenues for exploration. These include the following:

Separation of accounting and computation into different layers
Implementation of core components in highly modular functional code
Small groups of academics and developers competing with peer reviewed research
Heavy use of interdisciplinary teams including early use of InfoSec experts
Fast iteration between white papers, implementation and new research required to correct issues discovered during review
Building in the ability to upgrade post-deployed systems without destroying the network
Development of a decentralized funding mechanism for future work
A long-term view on improving the design of cryptocurrencies so they can work on mobile devices with a reasonable and secure user experience
Bringing stakeholders closer to the operations and maintenance of their cryptocurrency
Acknowledging the need to account for multiple assets in the same ledger
Abstracting transactions to include optional metadata in order to better conform to the needs of legacy systems
Learning from the nearly 1,000 altcoins by embracing features that make sense
Adopt a standards-driven process inspired by the Internet Engineering Task Force using a dedicated foundation to lock down the final protocol design
Explore the social elements of commerce
Find a healthy middle ground for regulators to interact with commerce without compromising some core principles inherited from Bitcoin

From this unstructured set of ideas, the principals working on Cardano began both to explore cryptocurrency literature and to build a toolset of abstractions. The output of this research is IOHK’s extensive library of papers, numerous survey results such as this recent scripting language overview as well as an Ontology of Smart Contracts, and the Scorex project. Lessons yielded an appreciation for the cryptocurrency industry’s unusual and at times counterproductive growth.





## Зачем нам ещё одна криптовалюта?



## Show me the code




WHY HASKELL?
The protocols that compose Cardano are distributed, bundled with cryptography and require a high degree of fault tolerance. On the best days, there will still be Byzantine actors, malformed messages and faulty clients unintentionally causing some form of havok on the network.

First, we wanted a language that enjoys a strong type system where we could easily use tools such as Quickcheck and more elaborate techniques such as Refinement Types while having a reasonable expectation of fault tolerance. An Erlang style OTP model satisfies the latter whereas languages like Haskell and Ocaml satisfy the former.

With the introduction of Cloud Haskell, Haskell gained many of Erlang’s advantages while not surrendering its own. Furthermore, Haskell’s modularity and composability has allowed us to use a lighter weight bespoke library called Time Warp for Cardano.

Second, Haskell’s libraries have evolved greatly over the last few years thanks to extensive work of commercial entities like Galois, FP Complete and Well-Typed. As a consequence, Haskell can be used to write production applications24.

Third, PureScript’s rapid evolution has provided a much needed bridge to the JavaScript world akin to what Clojurescript has given Clojure. We expect PureScript will be especially important when it comes to getting Cardano to work in a browser and developing mobile wallets.

Fourth, with respect to dependency resolution, Haskell in the last several years has enjoyed a significant social and technological effort led by technologists like Michael Snoyman through a platform called stackage that is both easy to use and well supported by FP Complete.

Fifth, beyond adequate dependency resolution, we aim for our software builds to be reproducible. In other words, with the same configuration values and dependency versions it should produce exactly the same build artifacts. Through stackage, we have been using NixOps to achieve reproducibility with great success.

Finally, the talent pool of developers specializing in Haskell is reasonably large — compared to its peers — and quite well-trained with the right mix of academic and industry credentials. It also acts as a competency filter as it is uncommon to find experienced Haskell developers without detailed knowledge of computer science.


;q



