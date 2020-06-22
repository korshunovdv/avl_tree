## AVL tree (named after inventors Adelson-Velsky and Landis) 
#### My implementation of AVL Tree, just for understanding algorithm


### Usage:

    # Create AVL Tree object
    my_tree = AVLTree()
    root = None
    # Add first root 10
    root = my_tree.insert(root, 10)
    root = my_tree.insert(root, 5)
    root = my_tree.insert(root, 15)
    # Let's imagine our current tree
    
    #         10                                        
    #        /  \                                        
    #       5    15                                                   

    root = my_tree.insert(root, 3)
    root = my_tree.insert(root, 4)
    # Now we are here.
    
    #       10            10             10   
    #      /  \          /  \           /  \  
    #     5    15 -->   5    15 -->    4   15 
    #                  /              / \     
    #                 3              3   5    
    #                  \                      
    #                   4                     

    root = my_tree.delete(root, 4) 
    
    # Deletion will look like thise

    #          10             10    
    #         /  \           /  \   
    #        4   15  -->    5    15 
    #       / \            /        
    #      3   5          3                                       

    root = my_tree.insert(root, 7)
    root = my_tree.insert(root, 8)
    
    # Let's look at rotation

    #         10              10               10              7      
    #        /  \            /  \             /  \            / \     
    #       5    15  -->    5    15  -->     7    15  -->    5   10   
    #      /               / \              / \             /   /  \  
    #     3               3   7            5   8           3   8    15
    #                          \          /                           
    #                           8        3                            

    root = my_tree.delete(root, 7)
    # We will delete our main root.

    #       7                8                                           
    #      / \              / \                                           
    #     5   10    -->    5   10                                                      
    #    /   /  \         /      \                                         
    #   3   8    15      3        15                                      
    #                                                   
    #                                            

    # Finally let's print ours tree to check ourselves.
    my_tree.print_tree(root)
