- **Listener**
	- using UnityEngine;
		public class BombEventBehaviour : MonoBehaviour
		
		{
		
		    public delegate void BombExplode(float range, Vector3 position);
		
		    [SerializeField] private float detectionRadius = 2f;
		
		    public static event BombExplode OnBombExplode;
		
		    // Start is called once before the first execution of Update after the MonoBehaviour is created
		
		    void Start()
		
		    {
		
		  
		
		    }
		
		  
		
		    // Update is called once per frame
		
		    void Update()
		
		    {
		
		        if (Input.GetKeyDown(KeyCode.E))
		
		        {
		
		            Debug.Log("Bomb exploded!");
		
		            OnBombExplode?.Invoke(detectionRadius, transform.position);
		
		        }
		
		    }
		
		}
- **Receiver**
	- using UnityEngine;
	public class OgreEventBehaviour : MonoBehaviour
	
	{
	
	    // Start is called once before the first execution of Update after the MonoBehaviour is created
	
	    void Start()
	
	    {
	
	        BombEventBehaviour.OnBombExplode += Explosion;
	
	    }
	
	  
	
	    void Explosion(float radius, Vector3 bombPosition)
	
	    {
	
	        if (Vector3.Distance(transform.position, bombPosition) < radius)
	
	        {
	
	            Destroy(gameObject);
	
	        }
	
	    }
	
	  
	
	    void OnDestroy()
	
	    {
	
	        BombEventBehaviour.OnBombExplode -= Explosion;
	
	    }
	
	}