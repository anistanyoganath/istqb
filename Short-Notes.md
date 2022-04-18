Testing is check the quality and reduce  the failure of the software

software that doesn't work properly leads to {
    loss of money time bussiness reputaion
    injury - death
}
test process {
    planning analyzing,
    designing,
    implementing test,
    reporting, 
    evaluating quality of test.
}
dynamic testing , static testing => execution of component system (1, 0);

Objectives of testing 
    prevent defects.
    verify all the requirements are working properly as the user expected
    functional fullfilled?
    build the confidence level of the quality of the object
    provide informations to stackkholder to make decesions.
    for legal requirements.

Component testing{
    find many  problems ASP
}
Acceptence testing{
    test  system working properly,
    passing informations to stackkholder
}

Testing(executing tests) & ISO/ICE/IEEE 29119-1
Debugging (fixing issues)

why  errors occuer?
    Time pressure
    Human fallibility
    Inexperienced project particiants
    Misscommunication between particiants
    unfamilliar technologies
    Environmental Condition (Radiation ElectroMagnaticField) => hardware issues

    false defetcs report (the way tests were executed)
    find root defect and sole it to prevent future issues

7 Testing Principles
    1.shows only presense of defects not absense
    2.exhausting testing is impossible
    3.early testing saves money and time
    4.defects cluster together
    5.Beware of the pesticide paradox
    6.Testing is context dependent{
        test~ e-commerce app | cricticl security system
    }
    7.Absesnse-of-errors is a fallacy



general aspects  of test process
    Test activities and task{
        planning
        
        monitoring & control

        analysis = What to test{
            type of defects {
                Ambiiguitios
                Omissions
                inconsistencies
                inaccuracies
                contractdiction
                Superfluous sttatments
            }
            }
        }
 
        design =how to test {
            designing testcases
            identifying necessary test data
        }

        implemetation = (do we have everything in place to runt the testt ?)
            setting up the Environment..


        execution (run test suits by schedule.)
            storing test IDs and  versions.
            compare results with expected results.
            logging  the outcome of execution.
            
        completion
            (collecting data from finished test..)
            check all the defect reports are closed.
            create a test sumery report for communicate with stackkholder.
            handover the testware

    }
    Test work product
        planning products (info abt basis)
        monitoring and control (repots )
        Test analysis (test Conditions)
        design products(test cases that excercise the test Condition)
        implementing w.product
            test procedures 
            test suits 
            execution schedule 
            (service virtulization auto test script ) used by system
        Test execution work products   
            status of  test cases (ready to run, pass, fail, blocked, skipped)
            defect report
            documentaion about used test tools, testware and tested object, items..
        Test completion work product
            Test sumerry report


    trasability between test basis and test work product
    

The psychology of Testing=========================
confirmation bias => its difficult to developers to accept the info mentioned in the test reports.. 

mindset of developers and testers
    dev => desgin and build a product
    tester => validating  the product


software Development Lifecycle Models{
    Sequential Development model | waterfall (
        by flow..
        testing will be done at final.
        require months or years for delivery to stackkholder
    )
    iterative and incremental DM | V-model{
        supports early testing
        features grow incremently
    }
}

No mater what model is choosen. test activities should start at the early stage of the Lifecycle.



Test Levels{
    Component Testing unit-testing{
        low risk
        findind defects that escaping from higher test level
        build confidence in component quality
        verify behaviors of the component
        usually perfomed by developer..

        test-basis{
            detailed desgin
            code
            data model
            component specification
        }
        test objects {
            component, units, modules
            code and data structure
            classes
            database modules
        }
        defects and failures{
            incorrect functionality
            data flow problems
            incorrect code and logic
        }
    }
    integration testing{
        verify functional and non -functional behaviors of interfaces are designed and specified
        building confidence in the quality of interfaces
        find defects on component|interface|system

        2 types of integration testing {
            component integration testing{
                responsibility of devs
                Defects [
                    incorrect | missing data
                    incorrect interface calls
                    interface mismatch
                    component communicate failures
                ]
            }
            system integration testing{
                responsibility of testers
                defects [
                    system communicate incorrect
                    interface mismatch
                    incorrect data encoding
                ]
            }
        }
        Test Basis work product{
            software and system design
            Sequence diagram
            interface , communicate protocol specification
            use cases
            Architecture at component or system Level
            workflows
            external interface definition
        }
        Test Objects{
            Subsystems
            databases
            Infrastructure
            interface
            Api
            Microservices
        }
        
    }
    system testing{
        focus on whole system or product.
        produce info that is used by stackkholder to make decesions.
        performed by independent testers.
        Objectives{
            validate that the system is complete and will work as expected..
            prevent defects from escaping to higher test level.
            building confidence in the quality of the whole system.
        }

        work products of test basis of sys testing{
            system and software requirements specification.
            risk analysis report
            use cases
            epic and user stories
            models of system behaviors
            state diagram
            system and user manual

        }

        Test objects of system testing{
            application
            hardware
            opearting system
            system under test (SUI)
            system config data
        }

        Defects{
            incorrect calculations
            unexcpected behaviors
            incorrect controls
            system failure
            system not worked as described in the manual
        }
        
    }
    Acceptence Testing{
        like sys testing, whole product test, work as expected?
        defects may not be found, if found it leads to major risk
        performed by coustomer bussiness users product owner

        common forms of Acceptence testing{
            user accept{
                build confidence that the user can use the system to meet their needs..
            }
            opeartioanl accept{
                work products [
                    backup and restore procedures
                    installation intruction
                    database packages
                    security standars or regulations
                ]
                performed by staff.
                focuses[
                    tesing of backup and restore
                    install uninstall upgrade
                    disaster recovery
                    user management
                    maintaince task
                ]
            }
            contractual and regulatory Acceptenc test{
                performed by user or independent tester
                contractual compliance archived ?
            }
            alpha and beta testing {
               used by devs of commercial off-the-shelf software
               performed by potential or exciting  coustomers

               building confidence amoung coustomers that the can use system under normal.
            }
        }

        work products of Acceptence testing{
            bussiness proocess 
            user or bussiness requirements
            regulations, legal contracts, standards
            use cases
            system requirements
            installation procedures

        }
        Test objects of Acceptence Tesing{
            system under test
            config data
            reports
            hot sites
            forms
            exciting and converted production data
        }
        Defects {
            system does not meet the user requirements
            bussiness rules are not implemented correctly
            system doesn't satisfy contractual requirements
            Non-functional failures
        }
    }
}

test first-approache => Test Driven Development (TDD)

Test types {
    Functional Test => what the system do?
    Non-Functional Test => how well the sys behaves
    White-Box Testing  => internal
    Change-related Testing => bug fixed ?(confirmation test) -> new bug? (regression test)

}

maintaince testing =>  when any change made it'll performed
trigged by new || modified things



Static Testing {
    testing without execution
    work products Test objects[
        specification, bussiness requirements
        functional requirements
        security requirements
        user stories
        code
        web pages
        contracts
        models
    ]

    Benifits of Static Testing {
        early detection of defetcs before dynamic test
        identifying defetcs which are difficult to do with dynamic
        increase Development productivity
        low cost and time
        lifetime 

    }
    difference from dynamic{
        directly identifying defects without executing
        with less efford can find defects
        internal quanlity 
    }
}

review process
    main activities {
        planning
        initial review
        individual review
        issue communication and analysis
        fixing and reporting   
    }

    roels of a typical formal review{
        Author
        management
        Moderator/ Faciliater
        Review Leader
        Reviewers
        Scribe/recorder   
    }


    informal{
        quickly solving miner problems
        not a documented process
        no meetings
        common in agile
        check-list is opt
    }
    walkthrough{
        meeting lead by Author
        scribe is mandatory (rec is important)
        check-list is opt
        defects logs produced

    }
    technical review{
        gaining consenses, detecting potential defects
        scribe is mandatory
        building confidence in the work product

    }
    inspection{
        follows a defined process with formal documented output and rules, checklist
        review meeting is required lead by Moderator
        author != leader/reader/scribe

        
    }


    Review Techniques {
        Ad hoc => no plan nor documentaion
        Checkklist-based => To-do
        Scenarios and dry runs {
            static
            fully structureed guidelines will be provided
        }
        perspective-based => focus on the point of view
        Role-based

    } 
choice of testing depends on
    complexity
    regulatory standards
    coustomer requirements
    risk Levels
    available docs
    tester skills
    available tools
    time and budget
    dev Lifecycle
    type of defects
    
testing Techniques
 Black-Box{
     external testing
     Dk code structure, inputs so difficult to plan testing
     privacy

     equivalence partitioning{
         valid values -> accepted by system  
         invalid values -> rejected by system
     }
     boundary value analysis BVA
     decesion table testing
     state transition testing
     use case testing


 }
 White-Box{
     knows internal code structure
     know what will be the inputs
     covers code-flow
     find bugs


     statement Testing and coverage{
         number of statements executed by the test / number of executable statements * 100
     }
     decesion testing
     no of decesions executed by the test / total no of  decesions
 }
 Experienced-base{
     testcases  detrived from tester's  skills

     Error Guessing{
         create a list of possible  errors
     }
     Exploratory system{
         use test sessions sheet to charter Objectives

     }
     Checkklist-based testing
 }
