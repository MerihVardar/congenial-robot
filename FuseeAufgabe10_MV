using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using Fusee.Engine.Core;
using Fusee.Math.Core;
using Fusee.Serialization;

namespace Fusee.Tutorial.Core
{
    public static class SimpleMeshes 
    {
        public static MeshComponent CreateCuboid(float3 size)
        {
            return new MeshComponent
            {
                Vertices = new[]
                {
                    // left, bottom, front vertex
                    new float3(-0.5f*size.x, -0.5f*size.y, -0.5f*size.z), // 0  - belongs to left
                    new float3(-0.5f*size.x, -0.5f*size.y, -0.5f*size.z), // 1  - belongs to bottom
                    new float3(-0.5f*size.x, -0.5f*size.y, -0.5f*size.z), // 2  - belongs to front

                    // left, bottom, back vertex
                    new float3(-0.5f*size.x, -0.5f*size.y,  0.5f*size.z),  // 3  - belongs to left
                    new float3(-0.5f*size.x, -0.5f*size.y,  0.5f*size.z),  // 4  - belongs to bottom
                    new float3(-0.5f*size.x, -0.5f*size.y,  0.5f*size.z),  // 5  - belongs to back

                    // left, up, front vertex
                    new float3(-0.5f*size.x,  0.5f*size.y, -0.5f*size.z),  // 6  - belongs to left
                    new float3(-0.5f*size.x,  0.5f*size.y, -0.5f*size.z),  // 7  - belongs to up
                    new float3(-0.5f*size.x,  0.5f*size.y, -0.5f*size.z),  // 8  - belongs to front

                    // left, up, back vertex
                    new float3(-0.5f*size.x,  0.5f*size.y,  0.5f*size.z),  // 9  - belongs to left
                    new float3(-0.5f*size.x,  0.5f*size.y,  0.5f*size.z),  // 10 - belongs to up
                    new float3(-0.5f*size.x,  0.5f*size.y,  0.5f*size.z),  // 11 - belongs to back

                    // right, bottom, front vertex
                    new float3( 0.5f*size.x, -0.5f*size.y, -0.5f*size.z), // 12 - belongs to right
                    new float3( 0.5f*size.x, -0.5f*size.y, -0.5f*size.z), // 13 - belongs to bottom
                    new float3( 0.5f*size.x, -0.5f*size.y, -0.5f*size.z), // 14 - belongs to front

                    // right, bottom, back vertex
                    new float3( 0.5f*size.x, -0.5f*size.y,  0.5f*size.z),  // 15 - belongs to right
                    new float3( 0.5f*size.x, -0.5f*size.y,  0.5f*size.z),  // 16 - belongs to bottom
                    new float3( 0.5f*size.x, -0.5f*size.y,  0.5f*size.z),  // 17 - belongs to back

                    // right, up, front vertex
                    new float3( 0.5f*size.x,  0.5f*size.y, -0.5f*size.z),  // 18 - belongs to right
                    new float3( 0.5f*size.x,  0.5f*size.y, -0.5f*size.z),  // 19 - belongs to up
                    new float3( 0.5f*size.x,  0.5f*size.y, -0.5f*size.z),  // 20 - belongs to front

                    // right, up, back vertex
                    new float3( 0.5f*size.x,  0.5f*size.y,  0.5f*size.z),  // 21 - belongs to right
                    new float3( 0.5f*size.x,  0.5f*size.y,  0.5f*size.z),  // 22 - belongs to up
                    new float3( 0.5f*size.x,  0.5f*size.y,  0.5f*size.z),  // 23 - belongs to back

                },
                Normals = new[]
                {
                    // left, bottom, front vertex
                    new float3(-1,  0,  0), // 0  - belongs to left
                    new float3( 0, -1,  0), // 1  - belongs to bottom
                    new float3( 0,  0, -1), // 2  - belongs to front

                    // left, bottom, back vertex
                    new float3(-1,  0,  0),  // 3  - belongs to left
                    new float3( 0, -1,  0),  // 4  - belongs to bottom
                    new float3( 0,  0,  1),  // 5  - belongs to back

                    // left, up, front vertex
                    new float3(-1,  0,  0),  // 6  - belongs to left
                    new float3( 0,  1,  0),  // 7  - belongs to up
                    new float3( 0,  0, -1),  // 8  - belongs to front

                    // left, up, back vertex
                    new float3(-1,  0,  0),  // 9  - belongs to left
                    new float3( 0,  1,  0),  // 10 - belongs to up
                    new float3( 0,  0,  1),  // 11 - belongs to back

                    // right, bottom, front vertex
                    new float3( 1,  0,  0), // 12 - belongs to right
                    new float3( 0, -1,  0), // 13 - belongs to bottom
                    new float3( 0,  0, -1), // 14 - belongs to front

                    // right, bottom, back vertex
                    new float3( 1,  0,  0),  // 15 - belongs to right
                    new float3( 0, -1,  0),  // 16 - belongs to bottom
                    new float3( 0,  0,  1),  // 17 - belongs to back

                    // right, up, front vertex
                    new float3( 1,  0,  0),  // 18 - belongs to right
                    new float3( 0,  1,  0),  // 19 - belongs to up
                    new float3( 0,  0, -1),  // 20 - belongs to front

                    // right, up, back vertex
                    new float3( 1,  0,  0),  // 21 - belongs to right
                    new float3( 0,  1,  0),  // 22 - belongs to up
                    new float3( 0,  0,  1),  // 23 - belongs to back
                },
                Triangles = new ushort[]
                {
                    0,  6,  3,     3,  6,  9,  // left
                    2, 14, 20,     2, 20,  8,  // front
                    12, 15, 18,    15, 21, 18, // right
                    5, 11, 17,    17, 11, 23,  // back
                    7, 22, 10,     7, 19, 22,  // top
                    1,  4, 16,     1, 16, 13,  // bottom 
                },
                UVs = new float2[]
                {
                    // left, bottom, front vertex
                    new float2( 1,  0), // 0  - belongs to left
                    new float2( 1,  0), // 1  - belongs to bottom
                    new float2( 0,  0), // 2  - belongs to front

                    // left, bottom, back vertex
                    new float2( 0,  0),  // 3  - belongs to left
                    new float2( 1,  1),  // 4  - belongs to bottom
                    new float2( 1,  0),  // 5  - belongs to back

                    // left, up, front vertex
                    new float2( 1,  1),  // 6  - belongs to left
                    new float2( 0,  0),  // 7  - belongs to up
                    new float2( 0,  1),  // 8  - belongs to front

                    // left, up, back vertex
                    new float2( 0,  1),  // 9  - belongs to left
                    new float2( 0,  1),  // 10 - belongs to up
                    new float2( 1,  1),  // 11 - belongs to back

                    // right, bottom, front vertex
                    new float2( 0,  0), // 12 - belongs to right
                    new float2( 0,  0), // 13 - belongs to bottom
                    new float2( 1,  0), // 14 - belongs to front

                    // right, bottom, back vertex
                    new float2( 1,  0),  // 15 - belongs to right
                    new float2( 0,  1),  // 16 - belongs to bottom
                    new float2( 0,  0),  // 17 - belongs to back

                    // right, up, front vertex
                    new float2( 0,  1),  // 18 - belongs to right
                    new float2( 1,  0),  // 19 - belongs to up
                    new float2( 1,  1),  // 20 - belongs to front

                    // right, up, back vertex
                    new float2( 1,  1),  // 21 - belongs to right
                    new float2( 1,  1),  // 22 - belongs to up
                    new float2( 0,  1),  // 23 - belongs to back                    
                },
                BoundingBox = new AABBf(-0.5f * size, 0.5f*size)
            };
        }

        public static MeshComponent CreateCylinder(float radius, float height, int segments)
        {   
            float3[] verts = new float3[5 * segments+1];
            float3[] norms = new float3[5 * segments];
            ushort[] tris = new ushort[segments * 5 * 3];
                                                                
            verts[0] = new float3(radius, height/2, 0);
            verts[segments] = new float3(0, height/2, 0);   
            verts[2 * segments] = new float3(radius, height/2, 0);   
            verts[3 * segments] = new float3(radius, -height/2, 0);  
            verts[5 * segments] = new float3(0, -height/2, 0);      

            norms[0] = new float3(0, 1, 0);
            norms[segments] = new float3(0, 1, 0);
            norms[2 * segments] = new float3(1, 0, 0);
            norms[3 * segments] = new float3(1, 0, 0);

            float delta = 2.0f * M.Pi / segments;

            for(int i = 1; i < segments; i++){
                float alpha = i * delta;

                verts[i] = new float3(radius * M.Cos(alpha), height/2, radius * M.Sin(alpha)); 
                norms[i] = new float3(0, 1, 0);

                verts[i + segments] = new float3(radius * M.Cos(alpha), height/2, radius * M.Sin(alpha));    
                norms[i + segments] = new float3(M.Cos(i * delta), 0, M.Sin(i * delta));

                verts[i + 2* segments] = new float3(radius * M.Cos(alpha), -height/2, radius * M.Sin(alpha));  
                norms[i + 2* segments] = new float3(M.Cos(i * delta), 0, M.Sin(i * delta));

                verts[i + 3* segments] = new float3(radius * M.Cos(alpha), -height/2, radius * M.Sin(alpha));
                norms[i + 3* segments] = -(float3.UnitY);

                tris[(i-1)*3+0] = (ushort) (i-1);
                tris[(i-1)*3+1] = (ushort) i;
                tris[(i-1)*3+2] = (ushort) segments;
                
                tris[(i-1)*3+9*segments+0] = (ushort) (3*segments+i-1);
                tris[(i-1)*3+9*segments+1] = (ushort) (3*segments+i);
                tris[(i-1)*3+9*segments+2] = (ushort) (4*segments);     

                tris[(i-1)*3+3*segments+0] = (ushort) (i+segments+1);
                tris[(i-1)*3+3*segments+1] = (ushort) (i+segments);
                tris[(i-1)*3+3*segments+2] = (ushort) (2*segments+i);   

                tris[(i-1)*3+6*segments+0] = (ushort) (2*segments+i);
                tris[(i-1)*3+6*segments+1] = (ushort) (2*segments+i+1);
                tris[(i-1)*3+6*segments+2] = (ushort) (segments+i+1);   
            }

            tris[(segments-1)*3+0] = (ushort) (segments-1);
            tris[(segments-1)*3+1] = (ushort) 0;
            tris[(segments-1)*3+2] = (ushort) segments;

            tris[(segments-1)*3+9*segments+0] = (ushort) (4 * segments -1);
            tris[(segments-1)*3+9*segments+1] = (ushort) (3 * segments);
            tris[(segments-1)*3+9*segments+2] = (ushort) (4 * segments);    

            tris[(segments-1)*3+3*segments+0] = (ushort) (segments + 1);
            tris[(segments-1)*3+3*segments+1] = (ushort) (2 * segments);
            tris[(segments-1)*3+3*segments+2] = (ushort) (3 * segments);    

            tris[(segments-1)*3+6*segments+0] = (ushort) (segments + 1);
            tris[(segments-1)*3+6*segments+1] = (ushort) (3*segments);
            tris[(segments-1)*3+6*segments+2] = (ushort) (2*segments+1); 

            return new MeshComponent{
                Vertices = verts,
                Normals = norms,
                Triangles = tris
            };
        }

        public static MeshComponent CreateCone(float radius, float height, int segments)
        {
            return CreateConeFrustum(radius, 0.0f, height, segments);
        }

        public static MeshComponent CreateConeFrustum(float radiuslower, float radiusupper, float height, int segments)
        {
            throw new NotImplementedException();
        }


        public static MeshComponent CreatePyramid(float baselen, float height)
        {
            throw new NotImplementedException();
        }
        public static MeshComponent CreateTetrahedron(float edgelen)
        {
            throw new NotImplementedException();
        }

        public static MeshComponent CreateTorus(float mainradius, float segradius, int segments, int slices)
        {
            throw new NotImplementedException();
        }

    }
}
